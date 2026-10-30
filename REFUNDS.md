# Rental returns and compensation

This policy distinguishes unused rental funds, service compensation, and withdrawals.
It accompanies the direct-return wallet and cooperative-cancellation client changes;
older clients may still require an explicit collection transaction.

## Unused funds

The rental deposit reserves a maximum budget; it is not a charge for the full period.
When a host settles, its authorized usage is paid, the agreed closing network fee is
burned, and the remainder returns to the rental key controlled by the funding wallet.
Confirmed, mature returns are included in that wallet's available funds automatically.
They can fund another rental or be withdrawn directly without an intermediate sweep.
Returns belonging to an automatic-renewal allowance wallet remain separate.

Stopping requests settlement; it is not confirmation of settlement. The payment agent
tracks the channel and submits the timeout refund when eligible if no host settlement
is confirmed. Keep the agent and its computer running until closure. The timeout is
specified by a block height, not a guaranteed wall-clock deadline. Confirmation and
node recovery can add delay. A failed or offline node must not be shown as a zero balance.

Available is a confirmed coin balance. Reserved-in-rentals and returning amounts are
estimates from the payment agent's journal, not additional spendable funds. They may
lag the chain, especially when the agent is offline; do not add them to Available.

## Cancellation before launch

A compatible host and renter can agree to a zero-usage cancellation before the host
has launched or accepted an ordinary payment state. The renter explicitly signs the
zero-usage state and the host signs the settlement. It returns the deposit minus the
agreed closing fee. Funding and closing fees remain network costs.

Cancellation also works after an unsuccessful startup if nothing launched or was
paid for. Older hosts may refuse this state; the renter then stops without it and
retains the existing timeout refund. An unavailable or uncooperative host cannot
prevent that timeout recovery, although a transaction still needs to be submitted
and confirmed. Cancellation never overrides payment for an already-started rental.

## Service complaints and fee responsibility

| Event | Automatic accounting | Compensation eligibility |
| --- | --- | --- |
| Voluntary early stop | Settle authorized usage and return the unused deposit | No automatic usage or network-fee reimbursement |
| Host never launches | Cooperative zero-usage close if supported; otherwise timeout refund | Verified host/CMFD fault: affected charges and unavoidable funding/closing fees may be reimbursed after review |
| Hardware fails the start check or differs from the listing | Stop; authorized check-window charges may already exist | Verified mismatch: affected check/usage charges and unavoidable funding/closing fees may be reimbursed after review |
| Provider downtime or incorrect charges | Stop further authorization when detected; settle or timeout | Verified affected interval or excess charges and unavoidable recovery fees may be reimbursed after review |
| Renter configuration or application error | Normal metered accounting | No automatic reimbursement |

Renters pay the disclosed on-chain fees at transaction time. Verified provider or
CMFD fault makes those unavoidable fees eligible for reimbursement; no on-chain
refund can reverse a fee already burned. Optional consolidation and ordinary
withdrawal fees are paid by the renter. Unused deposit return alone is not
compensation for charges already authorized. Lost profits, lost data, and consequential
losses have no automatic compensation under this operational policy.

## Filing and resolving a complaint

Report the rental ID, affected times, expected versus observed service, relevant
transaction IDs, and sanitized logs through CMFD marketplace support. The renter
client can also submit a signed report using `cmfd-rent report`; use `--help` for its
supported categories and arguments. Never submit private keys, seeds or passphrases.

Review must distinguish host/CMFD faults from renter errors and disputed evidence.
Record the decision, affected charges, fee amounts, evidence and reason. A compensation
payment requires a separate approved amount and verified destination, with a durable
payment record to prevent duplicates. Do not request another deposit to release a
refund. No automated compensation payout, guaranteed response time, or funded insurance
pool is claimed by this implementation.

This policy becomes user-facing through the renter wallet's “Returns, fees and service
complaints” panel when the updated package is distributed. Repository changes alone
do not deploy it to existing installations.

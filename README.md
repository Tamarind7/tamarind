Project Tamarind 🌴
An open-source testnet reference implementation for African cross-border remittance corridors on the Stellar network, demonstrating end-to-end integration with Stellar Ecosystem Proposals (SEPs).
📌 Overview
Cross-border payments across African corridors traditionally face high transaction friction, with fees averaging around ￼ USD per ￼ USD transferred alongside settlement delays spanning multiple days. While Stellar's payment infrastructure offers low-cost, near-instant settlement, building a compliant, working remittance flow requires standardizing client-to-anchor communications.
Project Tamarind serves as a complete reference implementation and client library that standardizes authentication, KYC data exchange, and interactive fiat off-ramping against anchor sandboxes using standard Stellar protocol interfaces.
🚀 Supported Stellar Ecosystem Proposals (SEPs)
1. SEP-10: Stellar Web Authentication
￼ Challenge-Response Cycle: Generates and parses cryptographic challenge transactions.
￼ JWT Issuance: Securely requests and verifies JSON Web Tokens (JWTs) required for authenticated anchor requests.
￼ Session Security: Manages token expiration and authentication persistence for client sessions.
2. SEP-12: Customer Information Service (KYC)
￼ Customer Registration: Submits structured user payload data using the ⁠putCustomer⁠ endpoint.
￼ Status Polling & Querying: Queries customer status via ⁠getCustomer⁠ to verify identity validation state (⁠NEEDS_INFO⁠, ⁠PENDING⁠, ⁠ACCEPTED⁠, ⁠REJECTED⁠).
￼ Callback Handling: Process status transitions required prior to transaction execution.
3. SEP-24: Hosted Deposit & Withdrawal
￼ Interactive Off-Ramp Protocol: Initiates interactive withdrawal flows against anchor endpoints.
￼ URL Handoff & Session Management: Opens and manages hosted anchor web views for seamless user data entry.
￼ Transaction Monitoring: Polls transaction status (⁠GET /transaction⁠) through lifecycle phases (⁠pending_user_transfer_start⁠, ⁠pending_anchor⁠, ⁠completed⁠).
￼ On-Chain Settlement: Executes USDC transactions on the Stellar network linked to local sandbox payouts.
🔄 End-to-End Remittance Sequence
📁 Repository Structure
🎯 Scope Boundaries
Functional Capabilities
￼ Single Corridor Off-Ramp: Pre-configured for standard African fiat currency settlement corridors.
￼ Sandbox Verification: Validates transaction hashes, status polling, and local rail payout simulations.
￼ Error & Exception Handling: Handles edge cases along interactive webview handoffs and network timeouts.
Explicitly Out of Scope
￼ Mainnet live currency settlement or real account funding.
￼ Multiple concurrent anchor corridors.
￼ Native mobile UI frameworks (focused strictly on core business logic and integration harness).
￼ Direct KYC vendor verification engine logic (handled externally by anchor).

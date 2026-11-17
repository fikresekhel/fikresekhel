## FikreSekhel

**Formal guarantees for security-critical code.**

I prove the properties that scanners and AI review can only estimate — on the
small, critical core where *probably safe* is not good enough: cryptography,
authorization, the money path, and the AI-generated code everyone is now
shipping. A 97%-precision scanner ranks the findings that exist. A proof rules
out the ones no tool was looking for.

**Focus**
- Formal verification — Lean 4, Dafny, SMT (Z3)
- Zero-knowledge circuit soundness — under-constrained circuits
- Verifying AI-generated code against the invariant it quietly breaks
- Cryptographic and high-assurance review

**[→ formal-guarantees](https://github.com/fikresekhel/formal-guarantees)** — a
series of machine-checked proofs, each catching a security bug that passes tests
and scanners:

| Bug caught by a proof | Tool |
| --- | --- |
| a wallet `withdraw()` that mints money | Dafny |
| an authorization check that leaks every tenant | Dafny |
| a confident LLM proof the kernel rejects | Lean |
| a 64-bit deposit that overflows away funds | Dafny |
| an under-constrained ZK circuit that proves a lie | Lean |

*Probabilistic tools find bugs. Proofs rule them out.*

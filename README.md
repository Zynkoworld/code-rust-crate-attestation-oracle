# zynko-oracle · `code-rust-crate-attestation-oracle`

**A deterministic, re-checkable attestation-integrity decider for the `code-rust-crate` knowledge domain.**

It decides, for a `code-rust-crate` knowledge capsule, whether it is a well-formed, provenance-carrying attestation (domain match, non-empty `kind` + `content`, present `provenance`, valid `content_hash`).

## Proven
Measured on a discriminating corpus (VALID + planted-INVALID), verified by running the oracle:

```
recall = 1.000    false_positives = 0    non-degenerate = yes  ->  PASS
```

`verify.py` (stdlib, no network) is the CI gate.

## Grounding (honest)
This is an **empirical structure + provenance integrity** oracle (fast-default ceremony), **not** a deep formal proof of the domain content. It certifies that a `code-rust-crate` capsule is well-formed and carries provenance -- one band of a multi-tier corpus (proven / reference / fast-default).

## License
Apache-2.0 (oracle code). Attested sources retain their own upstream licenses.

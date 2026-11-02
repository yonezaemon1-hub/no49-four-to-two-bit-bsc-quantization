# No.49 - Optimal Four-to-Two-Bit Quantization Through a Binary Symmetric Channel: A Finite Computer-Assisted Proof with an Equality Classification

**Ryutaro Yonezu - Independent Researcher**  
**Version:** v1.0 | **Date:** 2026-11-02  
**License:** All rights reserved  
**Proof:** Computer-assisted proof  
**Independent AI audit:** PASS (reported independent reproduction; not human peer review)  
**Novelty assessment:** INCONCLUSIVE  
**Peer review:** Not human peer-reviewed

## Publication files

**Zenodo Preprint:** [10.5281/zenodo.23875138](https://zenodo.org/records/23875138)  
**GitHub Release:** [v1.0](https://github.com/yonezaemon1-hub/no49-four-to-two-bit-bsc-quantization/releases/tag/v1.0)

The published PDF and ZIP were downloaded from both services after publication; all four SHA256 comparisons with the original files passed.

- [English preprint PDF](No49_v1.0_PREPRINT_20261102.pdf)
- [Reproducibility ZIP](No49_v1.0_REPRODUCIBILITY_20261102.zip)
- [SHA256 checksums](SHA256SUMS.txt)

## Result and scope

For X uniform on the four-dimensional Boolean cube, Y = X xor Z with independent Bernoulli(p) noise, and every quantizer Q from four bits to two bits,

`I(Q(X);Y) <= 2 (1 - h_2(p))` bits for `0 <= p <= 1/2`.

For `0 < p < 1/2`, equality holds exactly when the nonempty fibers partition the cube into four two-dimensional faces: 30 unlabeled partitions, or 720 maps with fixed output labels. At p=0, every four-equiprobable-output quantizer attains equality; at p=1/2, every quantizer does. The work is limited to n=4, k=2 and does not settle the general multibit conjecture.

## Reproduce the frozen certificates

Extract the ZIP, change to `No49_v1.0/audit_v0.2_frozen/`, and run:

```bash
python -B verify_no49.py
```

Python 3.10+ standard library only. On Windows:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File .\run_windows.ps1
```

The publication replay on 2026-11-02 passed:

```text
EXACT_P_1_4_PASS 396
ANALYTIC_ENDPOINTS_PASS 396 396
FULL_CERTIFICATE_REPLAY PASS; subsets=65535; orbits=401; noncube_orbits=396; intervals=31704; min_bound= 1.772151923623782e-14
```

Both SHA256 manifests passed (15 release entries and 10 frozen audit entries); all 16 extracted files were unchanged after replay. The proof uses exact integer arithmetic with outward logarithm bounds, together with analytic endpoint arguments. It is not a Lean/Coq formalization.

## Audit, provenance and prior-work limits

Computer-assisted proof. Independently reproduced by an AI auditor. The reported independent AI audit is PASS; the external auditor's independently written code and full execution log are not bundled. The publication replay above is a separate rerun of the supplied verifier. Not human peer-reviewed. Novelty assessment: INCONCLUSIVE.

**Full theorem-level comparison with Moazzeni (2026) remains incomplete.** The full text was not inspected, overlap with existing results has not been excluded, and no priority or novelty claim is made. See the paper for the references and limitations.

The manuscript and proof were developed with AI assistance under the author's direction. This is independent research, not an OpenAI publication or endorsement.

The audited mathematical code, frozen certificates and evidence data in the ZIP have not been changed. Historical files inside `audit_v0.2_frozen/` retain their original HOLD status because they record the earlier preparation stage; the author subsequently authorized this v1.0 publication.

Copyright (c) 2026 Ryutaro Yonezu. **All rights reserved**.

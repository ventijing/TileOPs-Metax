## Manifest status

![ops](https://img.shields.io/badge/ops-144-blue) ![implemented](https://img.shields.io/badge/implemented-128%20%2F%20144%20%2889%25%29-brightgreen) ![spec--only](https://img.shields.io/badge/spec--only-16-orange)

### Per-family coverage

| Family | Implemented | Spec-only | Total | Progress | Workloads |
| --- | ---: | ---: | ---: | --- | ---: |
| `attention` | 17 | 0 | 17 | `██████████` 100% | 70 |
| `convolution` | 2 | 4 | 6 | `███░░░░░░░` 33% | 40 |
| `elementwise` | 66 | 5 | 71 | `█████████░` 93% | 142 |
| `linear_attention` | 0 | 1 | 1 | `░░░░░░░░░░` 0% | 4 |
| `moe` | 7 | 0 | 7 | `██████████` 100% | 50 |
| `normalization` | 12 | 0 | 12 | `██████████` 100% | 50 |
| `pool` | 3 | 6 | 9 | `███░░░░░░░` 33% | 27 |
| `reduction` | 19 | 0 | 19 | `██████████` 100% | 47 |
| `scan` | 2 | 0 | 2 | `██████████` 100% | 4 |

### Spec coverage

| Field | Coverage |
| --- | ---: |
| `ref_api` | 144 / 144 (100%) |
| `roofline` (func or flops+bytes) | 144 / 144 (100%) |
| `source.kernel_map` | 104 / 144 (72%) |
| `source.bench_manifest_driven` | 124 / 144 (86%) |

**Workloads:** 434 total — 2.89 per implemented op.

### Conformance gaps

- Implemented ops without `kernel_map`: **34**
- Implemented ops without `roofline`: **0**
- Implemented ops without `source.bench_manifest_driven`: **5**
- Implemented ops with fewer than two workloads: **0**

<details><summary>Spec-only ops (16)</summary>

| | | |
| --- | --- | --- |
| `AlibiFwdOp` | `Conv2dBiasFwdOp` | `Conv2dFwdOp` |
| `Conv3dBiasFwdOp` | `Conv3dFwdOp` | `GatedDeltaNetPrefillFwdOp` |
| `GeluAndMulFwdOp` | `GeluTanhAndMulFwdOp` | `MaxPool1dFwdOp` |
| `MaxPool1dIndicesFwdOp` | `MaxPool2dFwdOp` | `MaxPool2dIndicesFwdOp` |
| `MaxPool3dFwdOp` | `MaxPool3dIndicesFwdOp` | `SiluAndMulFwdOp` |
| `SinusoidalFwdOp` |  |  |

</details>

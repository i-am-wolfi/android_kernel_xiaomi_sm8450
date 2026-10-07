# calcite-6.12 — marble / ukee (SM7475) sobre waipio

Base: `ltdq/android_kernel_qcom_sm8450-6.12#lineage-24.0` (6.11 Baby Opossum Posse,
tracking android16-6.12) + ACK + `i-am-wolfi/...-6.12#marble-wip a824e07`.
Tree 5.10.269 (`calcite` aa10e74) preservada em `xiaomi-backport-5.10/`.

## Commits (um por alteracao, sem perda)
- C1 base 6.11 (ltdq + ACK + marble-wip)
- C2 `arch/arm64/configs/marble_ukee.fragment` SEM LTO + `modules-lists/modules.list.marble`
- C3 `xiaomi-backport-5.10/` (drivers/configs 5.10 intactos, fora do Kbuild)
- C4 este doc + devicetrees (vendor/ ja vem da base)
- C5 `.github/workflows/build-marble-ukee.yml` (make direto, sem LTO)

## Plataforma
- waipio = SM8450, cape = SM8475, ukee = SM7475 (marble = Poco F5 / Redmi Note 12 Turbo).
- DTS: `vendor/qcom/devicetrees/qcom/diwali*.dts/dtso` da base (ukee reusa diwali, mesmo IP).
  Candidato recovery: `diwali-idp.dtb` + `diwali-idp-amoled-overlay.dtbo`.
- `arch/arm64/boot/dts/vendor -> ../../../../vendor/qcom/devicetrees` (ja na base).

## Build (Actions, sem LTO = mais rapido que thin-LTO)
`Actions -> build-marble-ukee-6.12` (push em `calcite-6.12` ou manual):
1. `merge_config gki_defconfig + marble_ukee.fragment` + `olddefconfig`
2. `make dtbs` fail-fast
3. `make Image.gz dtbs` com `ccache clang-19`
4. Artefato `marble-ukee-6.12` (Image.gz + dtb/dtbo + defconfig + modules.tar.zst)

Local: `scripts/kconfig/merge_config.sh -m arch/arm64/configs/gki_defconfig arch/arm64/configs/marble_ukee.fragment && make ARCH=arm64 LLVM=1 LLVM_IAS=1 olddefconfig && make ARCH=arm64 LLVM=1 LLVM_IAS=1 -j$(nproc) Image.gz dtbs`

# xiaomi-backport-5.10 (calcite)

Fontes 5.10.269 preservadas de `calcite` (aa10e74) para porte gradual ao 6.11/6.12.
NÃO compilados na base 6.11 (fora do Kbuild) — só referência.

- `marble_GKI.config`, `xiaomi_GKI.config`, `waipio_GKI.config`: fragments origem do C2.
- `modules.list.second_stage.marble`, `modules.list.vendor_dlkm`: origem do modules.list.marble.
- `drivers/input/fingerprint/*` (fpc_1540, goodix_3626/fod/tee): sem equivalente upstream no 6.11, precisa port.
- `drivers/input/touchscreen/goodix_9916*`: no 6.11 usar `TOUCHSCREEN_GOODIX_BERLIN_*` upstream até portar.

Próximos portes (um commit cada):
1. gt9916r -> berlin-i2c/spi
2. fpc1540 / goodix_3626 -> hid-spi / input/misc
3. MI_HW_ID, TOUCHFEATURE, BQ_FG, THERMAL_INTERFACE

## Сборка прошивок Padavan на серверах GitHub

Для личного использования

Каталог [`configs.release`](configs.release) содержит конфигурации маршрутизаторов для сборки публичных релизов

Создание публичного релиза прошивок: [Actions](../../actions) → [Make firmware releases](../../actions/workflows/make_release.yml)

Создание публичного релиза toolchain: [Actions](../../actions) → [Make toolchain release](../../actions/workflows/make_toolchain_release.yml)

Каталог [`configs.build`](configs.build) содержит конфигурации маршрутизаторов для сборки прошивок в артефактах

Создание артефактов: [Actions](../../actions) → [Build firmware](../../actions/workflows/build.yml)

В файле [`variables`](variables) указывается репозиторий прошивки, ветка, конкретный тег или коммит, ссылка на заранее собранный toolchain для экономии времени компиляции прошивки.
Если ссылку на toolchain не указывать, то он будет скомпилирован перед сборкой прошивки.

Конфигурации поддерживаемых роутеров перечислены здесь: [templates](https://github.com/nilabsent/padavan-ng/tree/master/trunk/configs/templates)

Так как не все шаблоны могут иметь актуальные параметры, стоит ориентироваться на образцы при составлении конфигурации в зависимости от размера флеш-памяти роутера:
- 4МБ: [ZyXEL Keenetic Start](https://github.com/nilabsent/padavan-ng/blob/master/trunk/configs/templates/zyxel/kn-start.config)
- 8МБ: [ASUS RT-N56U A1 Wireless Router](https://github.com/nilabsent/padavan-ng/blob/master/trunk/configs/templates/asus/rt-n56u.config)
- 16МБ и более: [ASUS RT-N56U B1 Wireless Router](https://github.com/nilabsent/padavan-ng/blob/master/trunk/configs/templates/asus/rt-n56ub1.config)

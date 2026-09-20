# TODO

## PoSoc

- [ ] Специфицировать T1 в PoSoc (пространство прикладных типов с доменными тегами): открыть пространство прикладных типов записей с доменным разделением тегов при валидации «подпись + каноническая форма + правило будущего» и семантике payload за приложением. Блокирует [specs/posoc-cdem.md](specs/posoc-cdem.md) (раздел 5) и [specs/app-state-model.md](specs/app-state-model.md) (раздел 9): без T1 невозможны ни перевозка прикладных записей CloDem, ни разделение общего хранилища на домены приложений. Реестры устройств ([specs/transport-identity.md](specs/transport-identity.md)) — ещё один потребитель T1.
- [ ] Собрать структуру спек PoSoc в main: разбивка на файлы из ветки wrong (concept/implementation/glossary) в main не собрана — там единый `specs/spec.md` (v0.13 → v0.14); при обновлении пина сабмодуля проверить, что все ссылки besoc на `../PoSoc/specs/spec.md` остаются валидными. См. PoSoc/TODO.md.

## specs/

- [ ] Починить незатронутые битые ссылки на старую структуру спек PoSoc в [specs/posoc-cdem.md](specs/posoc-cdem.md) и [specs/app-state-model.md](specs/app-state-model.md): ссылки вида `../PoSoc/specs/concept/*`, `../PoSoc/specs/implementation/*`, `../PoSoc/specs/glossary.md`, `../PoSoc/specs/index.md`, `../PoSoc/docs/posoc-*.md` указывают на файлы, не существующие после объединения спек PoSoc в единый `specs/spec.md`. Обновлены только места, затронутые разделением identity/device-ключей; остальные — по мере правок. При починке учитывать перенумерацию §7.3/§8 v0.14 (напр. [DEF-7.3.3] → §7.3.4).

## specs/index.md

- [ ] Добавить раздел про сабмодуль `GplVote` в `specs/index.md`: пин в `.gitmodules` есть (gpl-vote/GplVote), но в индексе спецификаций раздел отсутствует. Описать назначение репозитория и актуальное состояние спецификаций/документации для закреплённого коммита.

# Porsche Tools

Инструменты и исследования для Porsche PCM. Репозитории разделены по продуктам:

| Репозиторий | Назначение |
| --- | --- |
| [pcm-lab](https://github.com/porsche-tools/pcm-lab) | Общая лаборатория: эмулятор, подготовка среды, консоль и SD-образы; позднее — физический стенд. |
| [pcm-4-ge](https://github.com/porsche-tools/pcm-4-ge) | PCM **for Georgia**: грузинская локализация. |
| [pcm-cluster-display](https://github.com/porsche-tools/pcm-cluster-display) | Вывод и подмена изображения приборной панели. |
| [pcm-wireless-carplay](https://github.com/porsche-tools/pcm-wireless-carplay) | Штатный беспроводной CarPlay. |

**Согласованная схема зависимости:** push в `pcm-lab/main` → версионный GitHub Release с небольшим архивом инструментов → продукт скачивает нужный релиз при первом использовании.

В `lab.lock.json` продукта хранится только версия. Установка находится в его игнорируемой `.local/pcm-lab/`; общего кэша и зависимости от соседнего checkout нет. Новый релиз принимается изменением версии в lock.

Автоматическая доставка через релизы — следующий этап; сейчас используется закреплённый Git-checkout. Состояние и инструкции каждого направления находятся в его собственных `AGENTS.md`, `README.md` и `docs/STATUS.md`.

[pcm-legacy](https://github.com/porsche-tools/pcm-legacy) сохраняет общую историю до разделения. Прошивки, SDK, образы и частные данные остаются вне Git.

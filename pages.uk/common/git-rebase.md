# git rebase

> Повторно застосовує коміти з однієї гілки поверх іншої.
> Зазвичай використовується для дублювання комітів з однієї гілки до іншої, шляхом створення нових комітів у гілці призначення.
> Більше інформації: <https://git-scm.com/docs/git-rebase>.

- Перебазовує активну гілку поверх іншої, вказаної гілки:

`git rebase {{нова_базова_гілка}}`

- Розпочинає інтерактивне перебазування, яке дозволяє змінювати порядок, оминати, об'єднувати чи редагувати коміти:

`git rebase {{[-i|--interactive]}} {{цільова_базова_гілка_або_хеш_коміту}}`

- Продовжує перебазування перерване через збій злиття після виправлення конфліктних файлів:

`git rebase --continue`

- Продовжує перебазування призупинене через конфлікти при злитті, пропустивши конфліктний коміт:

`git rebase --skip`

- Перериває поточне перебазування (наприклад, якщо воно було перерване через конфлікт при злитті):

`git rebase --abort`

- Переносить частину поточної гілки поверх нової бази, використавши стару базу, як початок:

`git rebase --onto {{нова_база}} {{стара_база}}`

- Повторно застосовує останні 5 комітів, зупиняючись аби змінювати порядок, оминати, об'єднувати чи редагувати їх:

`git rebase {{[-i|--interactive]}} {{HEAD~5}}`

- Автоматично вирішує будь-які конфлікти надавши перевагу робочій версії гілки (ключ `theirs` має обернене значення в цьому випадку):

`git rebase {{[-X|--strategy-option]}} theirs {{назва_гілки}}`

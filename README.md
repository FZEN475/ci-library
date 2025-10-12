# ci-library
## Description

Библиотека ci для gitlab.

---
## [auto_merge](https://github.com/FZEN475/ci-library/blob/main/auto_merge/.gitlab-ci.yaml)
* Автоматическое объединение веток.
* Объединение только после успешного завершения тестов.
* Сжатие коммитов с последующей заменой на сообщение из последнего.
* Автоматическое перебазирование ветки источника.
* Автоматическое подписание.*
* Возможность удаления ветки источника после объединения.
### Variables
* `merge_branch_action` - удаление ветки-источника после объединения.
  ```yaml
    inputs:
      merge_branch_action:
        options: ['skip', 'delete']
        type: string
        default: 'skip'
  ```
* `$PROJECT_TOKEN`* - переменная группы gitlab с токеном пользователя с правами на подписание и объединение веток.

---
## [docker_build](https://github.com/FZEN475/ci-library/blob/main/docker_build/.gitlab-ci.yaml)
* Сборка образа и помещение в артефакты.
* Отправка образа в репозиторий.
### Variables
* `docker_builder` - подключение сборки.
```yaml
    inputs:
      docker_builder:
        type: boolean
        default: false
```

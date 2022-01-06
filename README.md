## Установка 

### Gitlab Pipeline exporter

1. Установка Docker и Docker-compose, ссылки на tutorial's: [Docker] and [Docker-compose]
2. Зайти на выделенный сервер через доступный ssh-client , создать директорию

```sh
mkdir gitlab-explorer
cd gitlab-explorer
```

3. склонировать данный репозиторий

```sh
git clone $REPOSITORY
```

4. Повторить действия из видео 
 - Создание токена 
 - Конфигурирование `gitlab-ci-pipelinex-exporter.yml`
 - Запуск compose  - `make up`
 
### Использование
`Grafana` - адрес машины\URL:3000

`Prometheus` - адрес машины\URL:9090

Пароль и логин по умолчанию для grafana - `admin`. После первой авторизации будет предложено сменить его.

Синтаксис для изменения конфигурации сбора метрик(файла `gitlab-ci-pipelinex-exporter.yml`) - [Syntax].

## Отступление

При желании вы можете использовать свои, уже имеющиеся Prometheus и Grafana, исправив конфиг и добавив дашборды.
Все конфигурации указаны в соответствующих директориях репозитория.

Используемые данные были взяты из [официального источника].


[Syntax]:<https://github.com/mvisonneau/gitlab-ci-pipelines-exporter/blob/main/docs/configuration_syntax.md>
[официального источника]:<https://github.com/mvisonneau/gitlab-ci-pipelines-exporter>
[Docker]:<https://docs.docker.com/engine/install/>
[Docker-compose]:<https://docs.docker.com/compose/install/>

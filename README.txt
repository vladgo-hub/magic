Magic - minimal Ionic/Angular project wrapper
--------------------------------------------
Что внутри:
- src/ : здесь находится ваш сайт (index.html, css/, js/, images/, fonts/, sass/)
- assets/ : копия css/, js/, images/, fonts/ в src/assets/ (для удобства настройки angular.json)
- ionic.config.json, package.json, angular.json, tsconfig.json : минимальные конфиги для Appflow

Важно:
- Этот проект — минимальный wrapper. Он НЕ является полноценным Angular приложением.
- Appflow/Angular CLI при попытке выполнить `ng build` могут потребовать полноценную Angular структуру.
- Если сборка через Appflow выдаёт ошибки, рекомендую один из вариантов:
  1) Создать локально проект `ionic start Magic blank --type=angular`, затем заменить src/ на содержимое твоего сайта и залить в репозиторий.
  2) В Appflow выбрать "Import existing project" и убедиться, что в разделе Build указаны правильные команды (возможно заменить `ng build` на `echo 'static build'` или использовать custom workflow).

Как дальше:
1) Разархивируй Magic_Ionic.zip
2) Проверь содержимое src/index.html — пути к css/js должны быть относительными (например: assets/css/...)
3) Залей полученную папку в репозиторий и подключи к Appflow как "Import existing project".

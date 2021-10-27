# Deploy app using Elastic Container Registry

##  Публикация image в Elastic Container Registry

1. В приложении выполнить **npm run publish:image**

В результате будет создан не оптимизированный image размером **440.54 MB**

Далее можно перейти в ветку __feat/deploy-from-registry__ и выполнить команду **npm run publish:image**. В результате будет создан оптимизированный image размером 20.21

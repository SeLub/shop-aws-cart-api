# Repository of Cart API service 

Backend: https://github.com/SeLub/shop-aws-be  
Frontend: https://github.com/SeLub/shop-aws-fe   
Task: https://github.com/rolling-scopes-school/nodejs-aws-tasks/blob/main/task8-docker-elastic-beanstalk/task.md  

Barnch: NON-optimezed Dockerfile https://github.com/SeLub/shop-aws-cart-api/tree/feat/nonopimized-deploy-from-registry
Barnch: optimezed Dockerfile https://github.com/SeLub/shop-aws-cart-api/tree/feat/deploy-from-registry

В ветке feat/nonopimized-deploy-from-registry находится НЕоптимизированный имидж. Если В приложении выполнить npm run publish:image, то в результате будет создан не оптимизированный image размером __440.54 MB__. Далее можно перейти в ветку feat/deploy-from-registry и выполнить команду npm run publish:image. В результате будет создан оптимизированный image размером __20.21 MB__.

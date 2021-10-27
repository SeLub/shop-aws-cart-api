# Deploy app using Elastic Container Registry

## Создание приложения

eb init -r eu-central-1

Enter Application Name: shop-aws-cart-api
It appears you are using Docker. Is this correct? Y

Select a platform branch.
1) Docker running on 64bit Amazon Linux 2
2) Multi-container Docker running on 64bit Amazon Linux (Deprecated)
3) Docker running on 64bit Amazon Linux (Deprecated)

Select = 1

Do you wish to continue with CodeCommit? (Y/n) n
Do you want to set up SSH for your instances? (Y/n) n



##  Действия: деплой приложения 

1. Создайте Dockerfile в корневой папке Dockerfiles
2. Откорректируйте скрипт build-and-publish.sh в папке scripts/docker
3. Откорректируйте скрипт deploy.sh в папке scripts/docker
4. Откорректируйте файл Dockerrun.aws.json в папке scripts/docker
5. eb create --single
	Enter Environment Name - вводим имя либо оставляем по дефолту
	Enter DNS CNAME prefix - вводим имя либо оставляем по дефолту
	Would you like to enable Spot Fleet requests for this environment? (y/N): N
6. Переходим в сервис Elastic Beanstalk, в соответствуt ющий только что созданный энвайронмент и выбираем пункт Go to environment и получаем ссылку на наше приложение. Либо ссылка доступна в сообщения в терминале:

2021-10-27 07:21:26    INFO    Application available at total-new-app.eu-central-1.elasticbeanstalk.com.
2021-10-27 07:21:26    INFO    Successfully launched environment: total-new-app


------
##  Публикация image в Elastic Container Registry

1. В приложении выполнить npn run publish:image


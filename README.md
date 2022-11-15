# stocKManagement
Components of Stock Management Frontend, Backend and Platform

Format to search the date in postman - 2022-11-03T04:27:55.521Z

Site to access the aws site deployed is,

http://deploy-stock.s3-website.us-east-2.amazonaws.com

The load balancer link which can be used in the place of environment of frontend is ,

http://load-balancer-final-1535937963.us-east-2.elb.amazonaws.com

API Gateway link is,

https://va8bq4r4u3.execute-api.us-east-2.amazonaws.com/stockDeploy

Site to understand how to create service, map a ecr image, task definition and load balancer to it...

https://www.youtube.com/watch?v=3Kr_455zMk4

Site to understand how to create task definition, map a docker image from docker hub, task definition under fargate and a single service task...

https://www.youtube.com/watch?v=z7_LdCVnCRU

Site to know the steps for deploying a front end built app (angular or react) into AWS S3 Bucket,

https://blog.cloudthat.com/step-by-step-guide-to-deploy-reactjs-app-on-aws-s3/

For API Gateway, there were steps followed,

1) get on to the api gateway and create new REST API.
2) after creating there will be resource tab for which we need to create resources from base for example api/v1.0/market/company and here for every name we need to add a resource, in the creation we can give any resource name and in path we can give api so it will create as /api.
3) enable the API Gateway CORS check button and create.
4) after created, click on the action button on top corner with the created resource,select the enable CORS and a screen will appear adjacent.
5) select the check boxes of default 4xx and defalut 5xx, then click on save,.
6) repeat the same for all the resource you create, and enable the cors after creating.
7) if the resource is a value which is being passed, enter the value with flower braces enclosed like '{value}'.
8) after the resource reaches the end, give create method and mention the get or post or delete option click the tick next to it.
9) a method creation screen appear, select the integration type as HTTP, endpoint url will be the loadbalancer url along with the entire get or post or delete call with parameter expection if present, then click on  save, also follow the enable cors from actions for tis too.
10) then click on actions, select deploy api create a new stage where it needs to be deploy then click deploy, it will generate a url which can be used for backend url to be inserted in the environment.ts file of frontend.

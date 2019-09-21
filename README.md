1. 解决Permission Denied

```yml
deploy_Staging:
  stage: deploy
  script: 
    - ls -lsa ./scripts
    - whoami
    - chmod +x ./scripts/RancherDeploy.sh
    - ./scripts/RancherDeploy.sh -k $RANCHERACCESS -s $RANCHERSECRET -a $STAGING_ID
  environment:
    name: Staging
    url: https://Staging.app.net
 ```

* [ ] Refine top README.md
* [ ] Set up circle.ci build
* [ ] set up `helm lint` in circle
* [ ] set up open api lint for each <service>-osb-service-definition.json
* [ ] Generate each <service>/Chart.yml from <service>-osb-service-definition.json
  * Reuse/submodule from https://github.com/orange-cloudfoundry/osb-to-helm-poc/  
* [ ] Generate each <service>/README.md from <service>-osb-service-definition.json
* [ ] Generate each <service>/values.yaml from <service>-osb-service-definition.json
* [ ] Generate each <service>/values.json.schema from <service>-osb-service-definition.json
* [ ] Set up execution of `helm install`, `helm test`, `helm uninstall` for each service
  * Inspiration from https://github.com/Orange-OpenSource/casskop/blob/master/.circleci/config.yml using https://github.com/rancher/k3d
* [ ] Generate and publish chart in a helm chart repo 
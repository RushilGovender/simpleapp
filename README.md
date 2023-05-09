The declarative yaml manifests in this repo are:
* `jade-shooter-deployment.yaml`: deploys a scalable `deployment` of a simple app which creates a scalable number of K8s `pod`s which respond to port 80 and encapsulate a container 
* `jade-shooter-service.yaml`: creates a `service` that allows this webapp's port 80 to communicate outside of its K8s namespace (AKA dedicated secure cluster) via port 8080
* `jade-shooter-ingress.yaml`: creates an `ingress` that exposes the `service` to requests outside of the K8s cluster at https://jade-shooter.rancher.localhost

## Usage
1. Install Rancher Desktop https://rancherdesktop.io/, the easiest way to get a local K8s lab imo.

2. Clone this repo 

    ```
    git clone https://github.com/RushilGovender/simpleapp.git
    ```

3. Apply the manifests in this repo 
 
    ```bash
    cd simplest-k8s/
    kubectl apply -f .
    ```

4. Browse to https://jade-shooter.rancher.localhost
    

## Notes
* The app is this customizable Kaboom space shooter created in this article: https://javascript.plainenglish.io/kaboom-js-repl-it-custom-top-down-shooter-in-5-min-ebad8157073a?postPublishedType=repub

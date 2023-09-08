# Helm-Charts

Helm charts are a package manager for Kubernetes applications. They are a way to define, install, and upgrade even the most complex Kubernetes applications. Helm charts are widely used in the Kubernetes ecosystem to simplify the deployment and management of applications on Kubernetes clusters.

## Here are some key points about Helm charts:

- Package Management: Helm charts package Kubernetes resources (such as deployments, services, configmaps, and more) into a single, versioned package. This package can be easily distributed and shared with others.

- Templates: Helm uses templates written in the Go templating language to allow users to customize Kubernetes manifests easily. This enables parameterization, where you can provide different values for various configurations, making your charts highly customizable.
- Reusability: Helm charts promote reusability by allowing users to define common Kubernetes objects and configurations as templates, which can then be used across multiple deployments or projects.

- Versioning: Helm charts have versioning support, so you can specify which version of a chart to install or upgrade to. This helps maintain consistency in your deployments.

- Dependency Management: Charts can depend on other charts, which allows for the creation of complex applications composed of multiple microservices or components. Helm handles dependency resolution and installation.

- Repository: Helm charts can be stored in Helm repositories, making it easy to share and distribute your applications with others. Helm comes with a default public repository called Helm Hub, but you can also set up your own private repositories.

- Release Management: Helm tracks the history of releases, making it easy to roll back to a previous version of an application if needed. This feature is crucial for managing updates and handling errors in a controlled manner.

- Security: Helm has built-in security features to ensure that charts and dependencies are signed and validated, reducing the risk of installing tampered or malicious charts.


# installation options for HELM

- from binary
  
    - Download your desired version
    - Unpack it (tar -zxvf helm-v3.0.0-linux-amd64.tar.gz)
   - Find the helm binary in the unpacked directory, and move it to its desired destination (mv linux-amd64/helm /usr/local/bin/helm)

- from script
    ``` 
    $ curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
    $ chmod 700 get_helm.sh
    $ ./get_helm.sh 
    ```

- Through package managers
  - From Homebrew (macOS) 
  `brew install helm`

  - From Chocolatey (Windows)
  `choco install kubernetes-helm`
  
  - From Scoop (Windows) 
   `scoop install helm`
  
  - From Apt (Debian/Ubuntu)
   ```
   curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
   sudo apt-get install apt-transport-https --yes
   echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
   sudo apt-get update
   sudo apt-get install helm
   ```
  - From Snap  
 `sudo snap install helm --classic`


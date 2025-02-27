## Hi there 👋

Here is a small repository for a nginx load balancing test under local minikube cluster.

 Three yaml manifests are deployed : deployment, ingress, service.

#### The goal is to expose a service outside via the ingress controller. The deployment has a small hello  world application and a pod IP output parameter.

Once the application is deployed and the ingress is reached by outside the page should return a message.

The test requires a tunnel between my local environment and the minikube. The following commands are necessary for the test once the yaml manifests are deployed:

- minikube addons enable ingress

- minikube tunnel

- for i in {1..20}; do curl -s http://localhost/; echo ""; sleep 0.5; done

The latter invokes the curl command x20 times.

![Captura de ecrã 2025-02-27, às 13 27 16](https://github.com/user-attachments/assets/916e950a-30d1-44b1-897a-1f38fea9e93c)

<!--
**el-leston/el-leston** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

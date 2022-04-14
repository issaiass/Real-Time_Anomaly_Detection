# Realtime Anomaly Detection System


<details open>
<summary> <b>Project Resume<b></summary>

The data platform we will create consists of three main components: a service that serves the anomaly detection model, the monitoring platform Prometheus, and Grafana (a tool that excels at visualizing monitoring dashboards). The anomaly detector will be an Isolation forest model trained with a curated and real dataset provided by the author’s organization and used in daily work to detect anomalous users. As part of the model development, we will visualize the anomalous decision boundary to understand its decisions better. This service, along with Prometheus and Grafana, will run inside multiple Docker components. To deploy them, we will use Docker Compose, which is a tool for defining and running multiple Docker images.


#### <b>Expected Outcome</b>
<p align="center">
<img src = "imgs/dataset_viz.PNG?raw=true" center=true width="85%"/>
<img src = "imgs/plotly_scatter.PNG?raw=true" center=true width="85%"/>
<img src = "imgs/histogram.PNG?raw=true" center=true width="85%"/>
</p>

</details>

<details open>
<summary> <b>Running the docerfile and starting the notebook<b></summary>

- Building the new container from the dockerfile folder
~~~
    docker build . -t issaiass/lp-jupyter:latest
~~~
- Run a new container from an image exposing the current folder
~~~
    docker run -d --name devtest -p 8888:8888 --mount type=bind,source="$(pwd)",target=/src issaiass/lp-jupyter    
~~~
- Next get from the logs 
~~~
    docker logs devtest
~~~
- Copy the token of the jupyter notebook first executing the log command and then copying the token link
~~~
    http://127.0.0.1:8888/?token=809e516fa4240841351910b14e5b094431125a7757f77cd9
~~~
- Run the Exploration notebook.

</details>

<details>
<summary> <b>Resume of Docker Commands<b></summary>

- For building the Dockerfile
~~~
    docker build . -t [user]/[image:tag]
~~~
- For starting a new container
~~~
    docker run -d --name [container_name] -p 8888:8888 [user]/[image:tag]
~~~
- For starting an interactive terminal for the container
~~~ 
    docker exec -it [container_name] bash
~~~
- For starting a created container
~~~
    docker start [container_name]
~~~
- For stoping a container
~~~
    docker start [container_name]
~~~
- For deleting docker images and volumes
~~~
    docker rm -vf $(docker ps -aq)
~~~
- For deleting docker images (all)
~~~
    docker rmi -f $(docker images -aq) 
~~~
- For mounting a new image
~~~
    docker run -d --name [container_name] -p 8888:8888 --mount type=bind,source="$(pwd)",target=/src [user/image_name]
~~~

</details>


<details>
<summary> <b>Video<b></summary>

We will made a youtube video later

<p align="center"> </p>
</details>


<details>
<summary> <b>Issues<b></summary>

- No issues

</details>

<details>
<summary> <b>Future Work<b></summary>

- After finishing the application we will see.

</details>

<details open>
<summary> <b>Contributing<b></summary>

Your contributions are always welcome! Please feel free to fork and modify the content but remember to finally do a pull request.

</details>

<details open>
<summary> :iphone: <b>Having Problems?<b></summary>

<p align = "center">

[<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" />](https://www.linkedin.com/in/riawa)
[<img src="https://img.shields.io/badge/telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/>](https://t.me/issaiass)
[<img src="https://img.shields.io/badge/instagram-%23E4405F.svg?&style=for-the-badge&logo=instagram&logoColor=white">](https://www.instagram.com/daqsyspty/)
[<img src="https://img.shields.io/badge/twitter-%231DA1F2.svg?&style=for-the-badge&logo=twitter&logoColor=white" />](https://twitter.com/daqsyspty) 
[<img src ="https://img.shields.io/badge/facebook-%233b5998.svg?&style=for-the-badge&logo=facebook&logoColor=white%22">](https://www.facebook.com/daqsyspty)
[<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" />](https://www.linkedin.com/in/riawe)
[<img src="https://img.shields.io/badge/tiktok-%23000000.svg?&style=for-the-badge&logo=tiktok&logoColor=white" />](https://www.linkedin.com/in/riawe)
[<img src="https://img.shields.io/badge/whatsapp-%23075e54.svg?&style=for-the-badge&logo=whatsapp&logoColor=white" />](https://wa.me/50766168542?text=Hello%20Rangel)
[<img src="https://img.shields.io/badge/hotmail-%23ffbb00.svg?&style=for-the-badge&logo=hotmail&logoColor=white" />](mailto:issaiass@hotmail.com)
[<img src="https://img.shields.io/badge/gmail-%23D14836.svg?&style=for-the-badge&logo=gmail&logoColor=white" />](mailto:riawalles@gmail.com)

</p

</details>

<details open>
<summary> <b>License<b></summary>
<p align = "center">
<img src= "https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-sa.svg" />
</p>
</details>

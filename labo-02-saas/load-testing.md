# Load testing

* [x] Add htop to your Linux vm

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption><p>Htop view</p></figcaption></figure>

![Alt text](../labo-01-git-flow/images/firefox_GRRaEPNaY6.png)

* [x] Add stress to your Linux vm and try to stress your cpu

<!---->

* [Stress documentation](https://www.golinuxcloud.com/stress-command-in-linux/)

<!---->

* [x] In two ssh windows, stress your vm and observe the CPU load with htop

```
sudo apt install stress
sudo stress --cpu  8 --timeout 20
```


<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Htop view with load on CPU</p></figcaption></figure>

* [x] Observer the CPU peak on NewRelic

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>CPU Peak on New Relic</p></figcaption></figure>


![Alt text](../labo-01-git-flow/images/firefox_ujIByvHGDr.png)

## [Docker] Prometheus + CAdvisor + Grafana  

- 경로 이동(```prometheus-grafana```) 후 명령어 입력  
```
$ docker-compose up -d
```

#### ports  
prometheus : 9090  
node-exporter : 9100  
alertmanager : 9093  
cadvisor : 8080  
grafana : 3000  

#### grafana ID/PW : admin/foobar  

#### prometheus  
![image](https://user-images.githubusercontent.com/35215836/140909140-d5112326-ad7d-4bc2-808e-c11ed3920dd6.png)  

#### grafana  
![image](https://user-images.githubusercontent.com/35215836/143385297-3cd05221-ee66-4a8f-92aa-83025feff323.png)  

#### cadvisor  
![image](https://user-images.githubusercontent.com/35215836/140909341-da830094-eb8e-49f3-9b3c-487600053e70.png)  

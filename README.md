# - 🔒 Projeto de Bolsas DevSecOps/AWS,  Compass UOL, abril 2025 🔒 -

## 📦 Desafio extra na AWS 📦

## 📜 0 - Breve resumo >
Uma "continuação" do [último desafio](https://github.com/JorgeAntero/Compass-Uol-Desafio-3-AWS), onde precisamos implementar regras de autoscaling. Projeto realizado em dupla com o [Danilo Lustosa](https://github.com/DaniloLustosa-eng)!  
> OBS: Apesar de uma "continuação", a arquitetura não necessita ser a mesma, portanto, não usamos o wordpress, bem como RDS e EFS.

---
## 🌐 1 - Criando a VPC >
### Novamente o primeiro passo foi criar a VPC, porém desta vez, optamos por criá-la pelo método "VPC e muito mais", que gera automáticamente as sub-redes, gateways e todo o resto necessário para o funcionamento dela:  

![Print um](/Prints/1.1.png)  
![Print dois](/Prints/1.2.png)  
![Print três](/Prints/1.3.png)  
![Print quatro](/Prints/1.4.png)  

---
## 🚔 2 - Configurando grupos de segurança >
### O segundo passo também segue como o último desafio, portanto, criamos os grupos de segurança necessários:  

![Print quinto](/Prints/2.1.png)  
![Print sexto](/Prints/2.2.png) 

---
## 👥 2 - Load Balancer >
### Para o terceiro passo, criamos o Load Balancer:  

![Print quinto](/Prints/2.1.png)  
![Print sexto](/Prints/2.2.png) 

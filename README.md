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
## 👥 3 - Load Balancer >
### Então seguimos para a criação do Load Balancer:  

![Print sétimo](/Prints/3.1.png)  
![Print oitavo](/Prints/3.2.png)  

>- Adicionamos um Listener na porta 8080 para evitar possíveis erros; 

![Print nono](/Prints/3.3.png)  

---
## 🧱 4 - Modelo de execução >
### Antes de criar o Auto Scaling, precisamos criar o modelo de execução: 

![Print décimo](/Prints/4.1.png)  
![Print onze](/Prints/4.2.png)  
![Print doze](/Prints/4.3.png)  

>- A diferença para o último projeto é que aqui precisamos criar uma interface de rede que permita a atribuição de um IP público automáticamente;

---
## 🤖 5 - Criando o Auto Scaling >
### E então criamos o Auto Scaling Group:  

![Print treze](/Prints/5.1.png)  
![Print quatorze](/Prints/5.2.png)  
![Print quinze](/Prints/5.3.png)  

>- Escolhemos nosso balanceador de carga e ativamos a mudança de zona, ignorando as não íntegras;  

![Print dezesseis](/Prints/5.4.png)  

>- Ativamos a verificação de integridade do ELB também; 

![Print dezessete](/Prints/5.5.png)  

>- Deixamos a capacidade desejada e minima como 1, e máxima como 3; 

![Print dezoito](/Prints/5.6.png)  

>- Até configurações adicionais, deixamos tudo padrão;
>- Em configurações adicionais ativamos a coleta de métricas de grupo no Cloudwatch;  

![Print dezenove](/Prints/5.7.png)  
![Print vinte](/Prints/5.8.png)  

>- As duas prints acima demonstram o funcionamento de tudo que foi criado até agora; 

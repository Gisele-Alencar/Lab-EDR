# Monitoramento de Segurança com Wazuh (EDR)

<p align="left">
  <img src="https://img.shields.io/badge/Wazuh-005571?style=for-the-badge&logo=wazuh&logoColor=white" alt="Wazuh"/>
  <img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu"/>
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux"/>
  <img src="https://img.shields.io/badge/Killercoda-20232A?style=for-the-badge&logo=linux&logoColor=white" alt="Killercoda"/>
</p>


## O que é este projeto?

Este projeto demonstra o funcionamento prático de um **EDR** (*Endpoint Detection and Response*), que funciona como uma câmera de segurança e um alarme instalado dentro de um servidor. Ao juntar o **Wazuh** (uma ferramenta de EDR real de mercado) com o ambiente em nuvem do **Killercoda**, o laboratório prova como um ataque se comporta nos bastidores de um sistema operacional e como usar uma plataforma centralizada para monitorar e descobrir incidentes.

## Como o Projeto foi Feito

Para montar esse laboratório prático 100% na nuvem sem precisar baixar nada no computador, usando essas duas plataformas:

• **Killercoda:** Usei duas abas do terminal. A **Tab 1** funcionou como o nosso servidor que foi monitorado, e a **Tab 2** funcionou como a máquina do atacante disparando os testes maliciosos.

• **Wazuh Cloud:** Funcionou como a nossa central de controle do SOC para acompanhar os gráficos e receber os alertas dos ataques em tempo real.

##


### *Cenário 1: Instalando o Agente do EDR na Máquina Alvo*
Comando executado no terminal da Tab 1 do Killercoda para instalar o programa do agente Wazuh e apontar para o endereço do nosso servidor em nuvem.

<img width="1365" height="560" alt="image" src="https://github.com/user-attachments/assets/f096bf20-7243-4c3a-93db-f3fc286dff06" />



### *Cenário 2: Verificando a Conexão com o Painel do SOC*
Painel do Wazuh Cloud mostrando que a máquina monitorada (Ubuntu) conectou perfeitamente e ficou com o status verde de "Ativo".

<img width="1365" height="658" alt="edr1" src="https://github.com/user-attachments/assets/beacb089-1adc-4fba-bacc-3e2598233d57" />



### *Cenário 3: Disparando e Detectando os Ataques nos Bastidores*
Segundo terminal simulando as ações reais do invasor, tentando adivinhar senhas via SSH de forma automática (força bruta), injetando comandos suspeitos e alterando o arquivo principal de usuários (/etc/passwd)

<img width="1366" height="532" alt="edr2" src="https://github.com/user-attachments/assets/94cd5391-6cd4-4deb-80cb-8f5388b480b9" />


## Aprendizado

A realização deste laboratório trouxe conhecimentos fundamentais sobre segurança defensiva e monitoramento de ativos:

• **Entendimento de Telemetria:** Compreensão prática de como os logs e eventos do sistema operacional (como falhas de login e alteração de arquivos) são gerados em segundo plano.

• **Funcionamento do EDR:** Aprendizado sobre como o agente coleta esses dados brutos na ponta e envia para um servidor centralizado organizar tudo em formato de alertas.

• **Análise de Ataques:** Visão real de como atividades maliciosas comuns (como força bruta via SSH) deixam rastros visíveis que podem ser caçados por um Analista de SOC.

##

<p align="center">© 2026 - Gisele Alencar</p>

# 🔐 Auditoria de sistemas com Medusa - Laboratório de Força Bruta (Kali + Metasploitable 2 + DVWA)
O objetivo deste projeto foi compreender as técnicas ofensivas e refletir sobre mitigação e boas práticas de segurança nos sistemas. Para isso, foi realizado, antes de tudo, a configuração de um ambiente controlado usando Kali Linux e Metasploitable 2, com foco na execução de ataques de força bruta utilizando a ferramenta Medusa.

<br>

# 1 - 🛠️ Ambiente:
* VM Usada: VirtualBox;
* SOs usadas: Kali Linux(atacante) e Metasploitable 2(Alvo);
* Explorações: FTP, DVWA, SMB;
* Ferramentas Para a Exploração: Nmap, Medusa, SMBClient;
* Configurando a placa de rede dentro da VM como: "Host-Only", tanto do Kali Linux quanto do Metaspoitable 2. <br>
        └── Isso garante que o ataque não saia para a internet real.

<br>

## 2 - 📝 Verificações iniciais:
- Verificação de ping entre os dois SOs; <br>
      └── Verifica se ambos estão se comunicando.

- Para saber o ip e realizar a verificação do metasploitable 2: 
  ``` bash
  ip a
  ```
- Após isso, anote o Inet e teste no Kali Linux.
  ``` bash
  ping -c 3 coloque o IP
   ```
  
- Criação de listas(Wordlists) no Kali Linux para a realização dos testes de força bruta; <br>
      └── Criou? Deu certo? Então está tudo ok. Deu erro e não criou? Reinicie o Kali antes de aplicar qualquer outro comando de verificação (Comigo funcionou).
      
<br>

## 🕵️‍♂️ Cenários de Ataques:
 **1º Etapa: Escanear possiveis portas abertas e o tipo de serviço:**
   ```bash
   nmap -sV -p 21,22,80,445,139 192.168.56.102
   ```
* **Resultado da análise:** Porta 21 (FTP) aberta, rodando o serviço `ProFTPD`.

<br>

![](https://i.imgur.com/WTLoFrq.png)

## 🔗 Compartilhe com a comunidade ❤

Por favor, se esse conteúdo te ajudou, compartilhe.

[![GitHub Repo stars](https://img.shields.io/badge/share%20on-twitter-03A9F4?logo=twitter)](https://github.com/Luhrodrigues45/Auditoria-de-forca-bruta) [![GitHub Repo stars](https://img.shields.io/badge/share%20on-facebook-1976D2?logo=facebook)](https://github.com/Luhrodrigues45/Auditoria-de-forca-bruta) [![GitHub Repo stars](https://img.shields.io/badge/share%20on-linkedin-3949AB?logo=linkedin)](https://github.com/Luhrodrigues45/Auditoria-de-forca-bruta)

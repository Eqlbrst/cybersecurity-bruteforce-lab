Laboratório de Força Bruta com Kali Linux e Medusa

Sobre o projeto

Este projeto foi desenvolvido como parte de um laboratório prático de **Cibersegurança**, com o objetivo de compreender, na prática, o funcionamento de ataques de força bruta e **password spraying**, além de analisar formas de prevenção e mitigação desses ataques.

Os experimentos foram realizados em um **ambiente controlado de laboratório**, utilizando meu notebook Linux e máquinas virtuais vulneráveis, evitando qualquer interação com sistemas ou serviços de terceiros.

Durante o laboratório, utilizei o **Kali Linux**, a ferramenta **Medusa** e ambientes propositalmente vulneráveis para simular diferentes cenários de autenticação e avaliar como credenciais fracas podem ser exploradas.



Objetivos

- Compreender o funcionamento de ataques de força bruta;
- Utilizar o Kali Linux em atividades de auditoria de segurança;
- Conhecer e utilizar a ferramenta Medusa;
- Realizar testes controlados contra serviços FTP;
- Automatizar tentativas de autenticação em aplicações web;
- Compreender o conceito de password spraying;
- Realizar enumeração de usuários em ambientes SMB;
- Identificar os riscos associados ao uso de senhas fracas;
- Analisar medidas de mitigação contra ataques de autenticação;
- Documentar tecnicamente os procedimentos e resultados obtidos.



Ambiente de laboratório

Os testes foram realizados em um ambiente isolado e controlado.

Ferramentas e tecnologias utilizadas

- **Linux** — sistema utilizado para realização do laboratório;
- **Kali Linux** — distribuição utilizada para as atividades de segurança;
- **Medusa** — ferramenta utilizada para testes automatizados de autenticação;
- **Metasploitable 2** — máquina virtual propositalmente vulnerável;
- **DVWA (Damn Vulnerable Web Application)** — aplicação web vulnerável utilizada para estudos de segurança;
- **Nmap** — utilizado para reconhecimento e identificação de serviços;
- **VirtualBox** — utilizado para gerenciamento das máquinas virtuais;
- **Wordlists** — utilizadas para os testes de autenticação.



Reconhecimento do ambiente

Antes da realização dos ataques simulados, foi realizado o reconhecimento do ambiente de laboratório para identificar os hosts disponíveis e os serviços expostos.

O **Nmap** foi utilizado para identificar portas abertas e serviços disponíveis na máquina vulnerável.

Essa etapa permitiu compreender a superfície de ataque antes da realização dos testes de autenticação.



2. Ataque de força bruta contra FTP

Foi realizado um teste controlado de força bruta contra o serviço **FTP** disponibilizado pelo ambiente vulnerável.

Para isso, foram utilizadas listas contendo possíveis usuários e senhas, juntamente com o **Medusa**, permitindo automatizar as tentativas de autenticação.

O objetivo do teste não foi causar indisponibilidade ou obter informações de terceiros, mas demonstrar como credenciais fracas podem ser descobertas quando um serviço não possui mecanismos adequados de proteção contra múltiplas tentativas de login.

Conceito explorado

**Brute Force:** tentativa sistemática de diferentes combinações de credenciais até encontrar uma combinação válida.



3. Teste de autenticação em aplicação web

Também foi utilizado o **DVWA (Damn Vulnerable Web Application)** para estudar ataques automatizados contra formulários de autenticação.

O DVWA foi desenvolvido justamente para permitir o estudo de vulnerabilidades web em um ambiente controlado.

Durante o laboratório, foram realizadas tentativas automatizadas de autenticação utilizando uma wordlist, permitindo observar na prática como aplicações sem mecanismos adequados de proteção podem ser suscetíveis a esse tipo de ataque.



4. Password Spraying e SMB

Outro cenário estudado foi o **password spraying** em ambiente SMB.

Diferentemente do brute force tradicional, no password spraying uma mesma senha é testada contra diversos usuários, reduzindo a quantidade de tentativas realizadas contra cada conta individual.

Antes dos testes, também foi realizada a identificação de possíveis usuários disponíveis no ambiente de laboratório.

### Diferença entre as técnicas



| Brute Force -> Muitas senhas são testadas contra uma conta 
| Password Spraying -> Uma ou poucas senhas são testadas contra várias contas 
| Credential Stuffing -> Credenciais obtidas de outros vazamentos são reutilizadas



5. Wordlists

Foram utilizadas wordlists simples para os testes, contendo possíveis nomes de usuários e senhas.
O uso de listas pequenas foi suficiente para demonstrar o funcionamento das técnicas sem a necessidade de utilizar grandes bases de credenciais.
As listas foram utilizadas exclusivamente dentro do ambiente de laboratório.



Mitigações

Os testes também permitiram analisar medidas que podem reduzir o risco de ataques de força bruta e password spraying.

Entre as principais medidas estão:

- Utilização de senhas fortes e únicas;
- Implementação de autenticação multifator (MFA);
- Limitação de tentativas de autenticação;
- Bloqueio ou bloqueio temporário de contas após múltiplas tentativas;
- Implementação de mecanismos de rate limiting;
- Monitoramento de eventos de autenticação;
- Utilização de SIEM para identificação de padrões suspeitos;
- Monitoramento de atividades anormais em serviços como SMB;
- Desativação de serviços que não são necessários;
- Aplicação de atualizações e correções de segurança;
- Utilização de políticas adequadas de gerenciamento de credenciais.


## ⚠️ Aviso de segurança

Todos os testes apresentados neste projeto foram realizados exclusivamente em **ambiente controlado e autorizado**, utilizando máquinas e aplicações destinadas a estudos de segurança.

As técnicas apresentadas não devem ser utilizadas contra sistemas, redes, aplicações ou contas sem autorização expressa do responsável.

Este projeto possui finalidade exclusivamente **educacional e de pesquisa em segurança da informação**.



Tecnologias utilizadas

Linux
Kali Linux
Medusa
Nmap
Metasploitable 2
DVWA
VirtualBox
FTP
SMB

Heitor Costa

Projeto desenvolvido como parte dos meus estudos práticos em **Cibersegurança**, com foco no desenvolvimento de conhecimentos em segurança ofensiva, análise de vulnerabilidades e medidas de proteção.

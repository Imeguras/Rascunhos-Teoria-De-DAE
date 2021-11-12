### Arquitetura de software 

**front-end**: gajo que trabalha nos visuais para os consumidores, UI's, interfaces, cli, etc...
**back-end**: gajo dos servidores, base de dados, processamento de info, etc...
**fullstack**: ele é da pilha inteira, a pilha sendo as camadas da estrutura do projeto q falamos na aula anterior

---

Uma boa arquitetura tem de ser flexivel tipicamente aguentar mais de 10 anos.
E dificil dizer se uma arquitetura e boa ou não pois esta depende do ambiente relacionado o contexto, nem sempre um spaggeti code é mau e nem sempre uma lasagna code e bom, nem sempre performance e o objetivo.

O que ela não é:

* Modelo de dados
* Arquitetura fisica onde o sistema vai executar(apesar de fazer parte)
* Detalhes do desenho/implementação

Que regras devemos ter em conta quando se pensa numa arquitetura de software

* Elementos isolados, exemplo being reactive
* Responsabilidades bem definidas, ie atribuir bem os trabalhos, ie dont do cansat
* Comunicam através de interfaces bem definidas
* Diminuir as dependencias entre elementos, ie don't create web dependencies ou estrelas melhor criar blocos de codigo e chapar-lhe 30 interfaces
* Tentar antecipar a mudança, ie por exemplo planear dinamic loading de livrarias
* Ligações assincronas sempre que possivel, ie signals, multithreading, schedulers all that stuff

---

#### Exemplos de estruturas comums:

**Core system/plugins** pattern:

* basicamente inclui Intellij, Minecraft servers, etc...

**Microservice** pattern(tem aparecido mais e mais ultimamente):

* basicamente tem se uma API que da route dos pedidos para varios micro serviços que existem em que cada um tem certos serviços e uma base de dados: ie AWS, kubernets, etc...

**Space-based** pattern:

* basicamente os processos e onde o codigo e executado e abstracted apesar de haver so um set de elementos estes são distribuidos por varios processing units

**Event-driven** pattern:

* basicamente javascript animations/events, e tudo drived por um scheduler central que controla e diz onde e que as coisas são processadas

**Pipe-line** pattern: 

* basicamente existe uma sequencia de processos em que para passar para o outro tem de se passar por certos filtros, tipo login/password, premium subscriptions, cors-filter, etc...

**Layered** pattern(e oq iremos falar mais durante o semestro): 

* basicamente o sistema e dividido em 3 camadas separadas, estas sendo: serviços de apresentação(PLL), Regras de negocio(BLL) e Serviços de dados (DAL)

---

Again na layered pattern não saltar layers, por exemplo não se deve fazer a validação da password(se funciona ou não, not talking validating wrong characters or empty strings) na front end

Beware of fake layering(basicamente InflatIO code) fazer conn("select stuff") idealmente existem duas funçoes separadas, tipo loadbyid -> selectbyid, da para testar se estão divididas se for possivel alterar radicalmente as tabelas, etc... e o data layer não for toda deitada ao lixo

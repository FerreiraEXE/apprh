README

Esse projeto tem como objetivo simplificar os registros de profissionais da área de recursos humanos, tendo como ideia principal permitir o cadastro de funcionários, seus dependentes, publicar vagas e permitir a adição de candidatos.

Há a possibilidade de preenchimento de informações como: Nome da vaga, Data de expiração da vaga, Salário e Descrição para o cargo, assim como, nome, data de nascimento e email do funcionário, com a possibilidade de adição de dependente. em vínculo.

Todos os processos estão flúidos, dês da cascata da exclusão, até o include para inclusão, utilizando as tecnologias de forma pensada e eficiente.

Para realizar a conexão ao banco de dados, acesse "DataConfiguration.java" e "application.properties", preenchendo com as informações da sua base de dados.


*Este projeto foi testado apenas em conexão mysql*


Será criada uma estrutura semelhante a abaixo:

+--------------------+
| Database           |
+--------------------+
| apprh              |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+

+-----------------+
| Tables_in_apprh |
+-----------------+
| candidato       |
| candidato_seq   |
| dependente      |
| dependentes     |
| dependentes_seq |
| funcionario     |
| funcionario_seq |
| vaga            |
| vaga_seq        |
| vagas           |
+-----------------+

**Comandos executados**
show databases;
use apprh;
show tables;


Estrutura do projeto: 

C:.
¦   .classpath
¦   .gitignore
¦   .project
¦   mvnw
¦   mvnw.cmd
¦   pom.xml
¦   README.txt
¦   
+---.mvn
¦   +---wrapper
¦           maven-wrapper.jar
¦           maven-wrapper.properties
¦           MavenWrapperDownloader.java
¦           
+---.settings
¦       org.eclipse.core.resources.prefs
¦       org.eclipse.jdt.core.prefs
¦       org.eclipse.m2e.core.prefs
¦       
+---src
¦   +---main
¦   ¦   +---java
¦   ¦   ¦   +---com
¦   ¦   ¦   ¦   +---AppRH
¦   ¦   ¦   ¦       +---AppRH
¦   ¦   ¦   ¦           ¦   AppRhApplication.java
¦   ¦   ¦   ¦           ¦   DataConfiguration.java
¦   ¦   ¦   ¦           ¦   
¦   ¦   ¦   ¦           +---controllers
¦   ¦   ¦   ¦           ¦       BuscaController.java
¦   ¦   ¦   ¦           ¦       FuncionarioController.java
¦   ¦   ¦   ¦           ¦       VagaController.java
¦   ¦   ¦   ¦           ¦       
¦   ¦   ¦   ¦           +---models
¦   ¦   ¦   ¦           ¦       Candidato.java
¦   ¦   ¦   ¦           ¦       Dependentes.java
¦   ¦   ¦   ¦           ¦       Funcionario.java
¦   ¦   ¦   ¦           ¦       Vaga.java
¦   ¦   ¦   ¦           ¦       
¦   ¦   ¦   ¦           +---repository
¦   ¦   ¦   ¦                   CandidatoRepository.java
¦   ¦   ¦   ¦                   DependentesRepository.java
¦   ¦   ¦   ¦                   FuncionarioRepository.java
¦   ¦   ¦   ¦                   VagaRepository.java
¦   ¦   ¦   ¦                   
¦   ¦   ¦   +---META-INF
¦   ¦   ¦           MANIFEST.MF
¦   ¦   ¦           
¦   ¦   +---resources
¦   ¦       ¦   application.properties
¦   ¦       ¦   
¦   ¦       +---static
¦   ¦       ¦   +---bootstrap
¦   ¦       ¦       +---css
¦   ¦       ¦               bootstrap-grid.css
¦   ¦       ¦               bootstrap-grid.css.map
¦   ¦       ¦               bootstrap-grid.min.css
¦   ¦       ¦               bootstrap-grid.min.css.map
¦   ¦       ¦               bootstrap-reboot.css
¦   ¦       ¦               bootstrap-reboot.css.map
¦   ¦       ¦               bootstrap-reboot.min.css
¦   ¦       ¦               bootstrap-reboot.min.css.map
¦   ¦       ¦               bootstrap.css
¦   ¦       ¦               bootstrap.css.map
¦   ¦       ¦               bootstrap.min.css
¦   ¦       ¦               bootstrap.min.css.map
¦   ¦       ¦               
¦   ¦       +---templates
¦   ¦           ¦   index.html
¦   ¦           ¦   mensagemValidacao.html
¦   ¦           ¦   
¦   ¦           +---funcionario
¦   ¦           ¦       dependentes.html
¦   ¦           ¦       formFuncionario.html
¦   ¦           ¦       listaFuncionario.html
¦   ¦           ¦       update-funcionario.html
¦   ¦           ¦       
¦   ¦           +---vaga
¦   ¦                   detalhesVaga.html
¦   ¦                   formVaga.html
¦   ¦                   listaVaga.html
¦   ¦                   update-vaga.html
¦   ¦                   
¦   +---test
¦       +---java
¦           +---com
¦               +---AppRH
¦                   +---AppRH
¦                           AppRhApplicationTests.java
¦                           
+---target
    +---classes
    ¦   ¦   application.properties
    ¦   ¦   
    ¦   +---com
    ¦   ¦   +---AppRH
    ¦   ¦       +---AppRH
    ¦   ¦           ¦   AppRhApplication.class
    ¦   ¦           ¦   DataConfiguration.class
    ¦   ¦           ¦   
    ¦   ¦           +---controllers
    ¦   ¦           ¦       BuscaController.class
    ¦   ¦           ¦       FuncionarioController.class
    ¦   ¦           ¦       VagaController.class
    ¦   ¦           ¦       
    ¦   ¦           +---models
    ¦   ¦           ¦       Candidato.class
    ¦   ¦           ¦       Dependentes.class
    ¦   ¦           ¦       Funcionario.class
    ¦   ¦           ¦       Vaga.class
    ¦   ¦           ¦       
    ¦   ¦           +---repository
    ¦   ¦                   CandidatoRepository.class
    ¦   ¦                   DependentesRepository.class
    ¦   ¦                   FuncionarioRepository.class
    ¦   ¦                   VagaRepository.class
    ¦   ¦                   
    ¦   +---META-INF
    ¦   ¦       MANIFEST.MF
    ¦   ¦       
    ¦   +---static
    ¦   ¦   +---bootstrap
    ¦   ¦       +---css
    ¦   ¦               bootstrap-grid.css
    ¦   ¦               bootstrap-grid.css.map
    ¦   ¦               bootstrap-grid.min.css
    ¦   ¦               bootstrap-grid.min.css.map
    ¦   ¦               bootstrap-reboot.css
    ¦   ¦               bootstrap-reboot.css.map
    ¦   ¦               bootstrap-reboot.min.css
    ¦   ¦               bootstrap-reboot.min.css.map
    ¦   ¦               bootstrap.css
    ¦   ¦               bootstrap.css.map
    ¦   ¦               bootstrap.min.css
    ¦   ¦               bootstrap.min.css.map
    ¦   ¦               
    ¦   +---templates
    ¦       ¦   index.html
    ¦       ¦   mensagemValidacao.html
    ¦       ¦   
    ¦       +---funcionario
    ¦       ¦       dependentes.html
    ¦       ¦       formFuncionario.html
    ¦       ¦       listaFuncionario.html
    ¦       ¦       update-funcionario.html
    ¦       ¦       
    ¦       +---vaga
    ¦               detalhesVaga.html
    ¦               formVaga.html
    ¦               listaVaga.html
    ¦               update-vaga.html
    ¦               
    +---test-classes
        +---com
            +---AppRH
                +---AppRH
                        AppRhApplicationTests.class

(Estrutura extraída com o plugin 'Eclox')

Transparência:

Projeto para a atividade sobre Spring Boot do professor Elenilton Dezengrini referente a matéria 'Métodos de desenvolvimento'.

Este projeto foi realizado por Ana Flávia Lunedo e Gabriel Ferreira dos Santos, com apoio de Brian Lucas e do professor Jefferson Eduardo Guido, para ajudar na resolução de problemas.

Este projeto foi feito com a ajuda de tutoriais no YouTube, especialmente utilizando as aulas do professor Arthur A. Ferreira, onde ele mostra os conceitos e processos para a criação de um sistema semelhante ao publicado.

Contato:
gfsantos4@minha.fag.edu.br
aflunedo@minha.fag.edu.br

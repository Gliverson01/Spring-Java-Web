## Spring-java-web

### Todo o projeto foi feito com auxílio dessa vídeoaula

[![DevSuperior no Youtube](https://raw.githubusercontent.com/devsuperior/bds-assets/main/ds/yt-icon.png)](https://www.youtube.com/watch?v=D4frmIHAxEY)


 Programação orientada a objetos (qualquer linguagem)
               
            Ferramentas
            Spring Tool Suite (STS)
            Postman
  
### Visão geral do sistema

Vamos construir um pequeno sistema (API REST) de usuários e departamentos, com os seguintes casos de uso:

            Buscar todos usuários
            Buscar um usuário pelo seu id
            Inserir um novo usuário
            
   
   ![image](https://user-images.githubusercontent.com/74027319/150174562-7eff0c02-db7c-4b22-9e4e-b07192a723ea.png)
   
### Desenvolvimento moderno: relacional -> objeto -> json
  
   ![image](https://user-images.githubusercontent.com/74027319/150174776-e400dc60-f62d-4c47-ac29-8c44b8268088.png)
   
### Passos do projeto

    Criar o projeto
    Implementar o modelo de domínio
    Mapeamento objeto-relacional com JPA
    Configurar o banco de dados H2
    Criar os endpoints da API REST

### Trechos de código para copiar

#### Configuração do Maven Resources Plugin

```xml
<plugin>
	<groupId>org.apache.maven.plugins</groupId>
	<artifactId>maven-resources-plugin</artifactId>
	<version>3.1.0</version>
</plugin>
```
#### Configurações do banco de dados

```
# Dados de conexão com o banco H2
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=
# Configuração do cliente web do banco H2
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console
# Configuração para mostrar o SQL no console
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

#### Script SQL

```sql
INSERT INTO tb_department(name) VALUES ('Gestão');
INSERT INTO tb_department(name) VALUES ('Informática');
INSERT INTO tb_user(department_id, name, email) VALUES (1, 'Maria', 'maria@gmail.com');
INSERT INTO tb_user(department_id, name, email) VALUES (1, 'Bob', 'bob@gmail.com');
INSERT INTO tb_user(department_id, name, email) VALUES (2, 'Alex', 'alex@gmail.com');
INSERT INTO tb_user(department_id, name, email) VALUES (2, 'Ana', 'ana@gmail.com');
``` 
## Visão final do projeto
![image](https://user-images.githubusercontent.com/74027319/150177246-b534adc0-b30d-4a8a-b902-edbe86067dac.png)





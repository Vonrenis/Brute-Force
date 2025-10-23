# Brute-Force
Um estudo sobre ataques de força bruta
Primeiramente vamos inicar falando o básico,
O que seria um ataque de força bruta?
Nada mais nada menos que vocẽ tentar varias senhas várias vezes, existindo vários metodos como "password spraying",
consiste em vocẽ usar a mesma senha em diversos usuários ao mesmo tempo muitas vezes empregando um delay para ficar mais realista
Mas fica a dúvida Quanto tem de delay? bom nesse artigo do cgu que busca as informações da OWASP diz de 5 a 10 tentativas (Imagem 1)
Entretanto isso é eficaz de alguma forma?
Dependendo se for um servidor mais antigo pode ser que funcione
E que tipo de ferramenta é usada?
Uma ferramenta muito famosa utilizada no mundialmente famoso Kali linux é a medusa
O que a medusa faz? como que ela age?
Ela usa uma wordlist de nomes de usuários e senha mais comuns, sendo essa wordlist podendo ser uma que vocẽ mesmo criou ou pegou em algum lugar
sendo relativamente fácil de encontrar até mesmo aqui no github com milhares de senhas comuns e ou vazadas
Através de um comando: "medusa -h 'IP' -U lista_de_usuários - P lista_de_senhas ftp -t 6"
Só que o meu foco aqui nesse readme é falar como isso afeta as aplicações web
A mesma ferramenta citada acima, a medusa, pode ajudar a implementação de segurança nesses casos 
Porém primeiro precisamos saber qual tipo de bug é
A organização da OWASP disponibiliza o top 10 bugs web, no momento que eu escrevo esse readme só estou com acesso ao de 2021 sendo o de 2025 marcado para lançar em meados de novembro de 2025
Apesar de ter sido dito na aula que o pode ser um erro de CSRF, na verdade é um erro de AUT FAILURES
CRSF a grosso modo é forçar o navegador a autenticar e executar açoes que o atacante quer (imagem 2)
e o AUT falilures é justamente falhas de autenticação (imagem 3)
sendo muito mais compativel com a medusa pois uma dass falhas é nao proibir o usuário depois de X tentaticas
Foi confundido dessa maneira por causa  da maneira como era escrito na OWASP
Entretanto hoje com uma maior pesquisa e melhor adequação das categorias 
Sendo assim a relação da medusa e dos ataques de brute force com vulnerabilidades web são authentication failures
As imagens (4 e 5) mostram como esta escrito no site oficial do OWASP 2021
Tendo também a imagem 6 mostrando como a medusa se comporta em ambientes HTTP
Considerações finais 
Após disso tudo que foi dito vimos que a ferramenta medusa muito conhecida também pode ser utilizada em aplicações web
Referencias: https://repositorio.cgu.gov.br/bitstream/1/94451/1/Suene_artigo_final.pdf https://portswigger.net/web-security/authentication https://portswigger.net/web-security/csrf
http://foofus.net/goons/jmk/medusa/medusa-http.html https://owasp.org/www-project-top-ten/

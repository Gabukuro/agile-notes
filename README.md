# Prova

## 1. User Stories (4pontos)
- a) Defina o que é uma User Story e qual é sua finalidade no desenvolvimento de software ágil.<br>
R: User Story, ou História de Usuário, é uma prática onde o usuário final especifica informalmente uma funcionalidade que necessita no sistema, dizendo o que e para que quer. Sua finalidade é dar contexto para o desenvolvedor, informando o porquê do que eles estão desenvolvendo.

- b) Dada a seguinte demanda do cliente: "Um cliente deseja pesquisa rprodutos no e-commerce por nome possibilitando encontrá-los rapidamente". Escreva uma User Story adequada para essa demanda, incluindo critérios de aceitação. <br>
R: Como cliente, eu quero pesquisar produtos na plataforma de e-commerce por nome, para que eu possa encontrá-los rapidamente.

- c) Crie 2 histórias de usuário adicionais para este cenário do e-commerce, incluindo critérios de aceitação.<br>
R1: Como cliente, eu quero adicionar produtos na minha lista de desejo, para que eu possa centralizar os produtos que eu quero.<br>
R1: Como cliente, eu quero informar meu cep, para visualizar o preço de frete e tempo de entrega.

- d) Leia atentamente a seguinte User Story. Apresente possíveis critérios de aceitação: <br> "Como gerente de vendas, desejo gerar relatórios mensais de vendas para analisar o desempenho dos produtos." <br>
R: Eu quero visualizar um comparativo o desempenho de produtos do mês atual e do mês anterior.<br>
Eu quero filtrar o desempenho de produtos por nome.<br>
Eu quero exportar os dados do relatório em formato csv.<br>
Eu quero ter a visualização de desempenho de produtos por mês, trimestre e semestre.

## 2. Considerando uma função que inverte uma string nomeda string_invert. O pseudo código está abaixo (3 pontos)
```
FUNÇÃO string_invert(s) RETORNA string:
	DECLARE str_invertida = ""
	PARA CADA caractere c EM s DE TRÁS PARA FRENTE FAÇA:
		str_invertida += c
	FIM PARA
RETORNE str_invertida
FIM FUNÇÃO
```

Escolha entre JUnit, PyTest, Jest ou qualquer outra alternativa de teste unitários que preferir.<br>
Criar testes para:<br>
- a) strings vazias,<br>
- b) strings com um único caractere e<br>
- c) strings mais que um caractere.

```js
describe('Question 2', () => {
	it('a) should return empty string', () => {
		expect(string_invert("")).toBe("");
	});
	it('b) should work with string with only one character', () => {
		expect(string_invert("e")).toBe("e");
	});
	it('c) should invert all string', () => {
		expect(string_invert("serei invertido 😳")).toBe("😳 oditrevni ieres");
	});
});
```

## 3. Dado o seguinte teste unitário escrito em pseudocódigo(3pontos):
``` 
Teste "verificarContagemDeCaracteres" :
    resultado = contarCaracteres("Live long & prosper")
    verificarSe(resultado é igual a 18)
```
- a) Escreva uma possível função contarCaracteres (str) que atenda a esse teste. Use a linguagem que estiver mais habituado.
```js
const contarCaracteres = (word) => {
    return word.length
}
```

- b) Escreva pelo menos 1 outro teste unitário para afunção contarCaracteres (str)
```js
describe('contarCaracteres tests', () => {
    it('should handle an empty string', () => {
        expect(contarCaracteres('')).toBe(0);
    });
    it('should handle strings with n length', () => {
        expect(contarCaracteres('pneumoultramicroscopicossilicovulcanoconiótico')).toBe(46);
        expect(contarCaracteres('Azpilicuetagaraicosaroyarenberecolarrea')).toBe(40);
        expect(contarCaracteres('Sünnipäevanädalalõpupeopärastlõunaväsimatus')).toBe(43);
    });
});
```
<hr>

# Recuperação

- 1.1) R: A alternativa certa é a C
- 1.2) R: A alternativa C está correta pelo fato de que ela é a única que respeita o ciclo do TDD, onde é escrito o teste primeiro, ele deverá falhar (🔴), em seguinda deve-se escrever apenas o código necessário para passar os testes (🟢), então deve-se refatora o código (🟡) e assim por diante.
- 2.1) Exemplo de epic: `Melhorar a funcionalidade de pesquisa em um site de comércio eletrônico`, como eu dividiria em alumgas user sotries:
    - Como usuário, eu quero poder pesquisar produtos pelo nome para encontrar rapidamente o que estou procurando.
    - Como usuário, eu quero poder refinar minha pesquisa usando filtros, como categoria, faixa de preço e classificação.
    - Como usuário, eu quero ver resultados de pesquisa relevantes e organizados por relevância.
- 2.2) Os critérios de aceitação são importantes nas user stories porque definem requisitos claros, garantem transparência e facilitam a validação, ajudando a equipe a entender quando uma história está pronta e o cliente a avaliar o valor entregue. Para melhor entendimento, uma poesia sobre o tema:
    ```
    Critérios de aceitação, sem confusão,
    Clareza e transparência, essa é a lição.
    Testar o que é preciso, sem enrolação,
    Entregar valor, essa é a missão.
    ```
- 3.1) Um teste unitário é uma técnica de teste de software em que unidades individuais ou componentes de código são testados de forma isolada para garantir que funcionem conforme o esperado. Seu objetivo principal é verificar se cada parte do código funciona corretamente e detectar eventuais erros ou comportamentos inesperados. Para melhor entendimento, uma poesia sobre o tema:
    ```
    Teste unitário, no código eu vou dar uma olhada,
    Pra ver se tá redondo, sem deixar nada de lado.
    O objetivo é garantir, no jeito gaúcho de ser,
    Que o código funcione direito, como deve acontecer.
    ```
- 3.2) "Mocking" em testes unitários é a prática de criar objetos simulados (mocks) para representar partes do sistema real. Isso permite isolar a unidade de código sendo testada, controlando o comportamento dos componentes externos e verificando interações. Sem rimas dessa vez, a resposta ficou clara.
- 4.1) No Extreme Programming (XP), a refatoração é uma prática fundamental, pois ajuda a manter o código flexível e fácil de dar manutenção, promovendo a evolução contínua do software.
- 4.2) A programação em pares é uma prática em que dois programadores trabalham juntos em uma mesma tarefa ou código. Isso promove a colaboração, reduz erros, melhora a qualidade do código e facilita a transferência de conhecimento entre a equipe. A seguir um dueto inesperado para elucidar o tema:
    ```
    - Parça, falar de programar em dupla é de lei,
    Unir as mentes, é o que eu vou te dizer, meu rei.
    - Exato, meu amigo, sem rodeio nem lorota,
    Trabalhar lado a lado, não tem quem bote a pata.
    - Menos erro, mais qualidade, é o nosso caminho,
    Programar juntos, nosso destino e nosso carinho.
    - Na troca de ideias, a gente se aperfeiçoa,
    A parceria na programação, é a nossa escolha.
    - Código mais limpo, menos treta, sem drama,
    Com o camarada do lado, a programação se inflama.
    - É isso aí, meu chapa, colaboração é vital,
    Programação em par, é nosso jeito original.
    - Então, seguimos firmes, sem desviar da razão,
    Programação em par, é a nossa tradição!
    ```
- 4.3) O desenvolvimento orientado a testes é uma metodologia, que foi introduzida inicialmente pelo XP (Extreme Programming), a qual prega que os testes devem ser escritos antes da codificação propriamente dita.
- 5.1) Métricas-chave incluem velocidade da equipe, satisfação do cliente, qualidade do código, cumprimento de práticas ágeis e cumprimento de prazos para avaliar o sucesso de implementações de Scrum ou XP. A seguir a explicação como se fosse um RPG:
    ```
    No "Scrum RPG," somos heróis do desenvolvimento, mas uma ameaça misteriosa paira sobre nós. Planejamos sprints, enfrentamos quests (projetos), cada membro tem habilidades únicas. O chefão (cliente) cobra resultados, XP extra com artefatos mágicos. Foco sob essa sombra enigmática, a jornada continua.
    ```
- 5.2) User Stories e Epics são usadas para representar funcionalidades de forma simples e compreensível. Isso ajuda a alinhar as expectativas dos stakeholders não técnicos e facilita a comunicação com a equipe de desenvolvimento. Para encerrar, gostaria de deixar o seguinte poema respondendo a questão:
    ```
    Em tempos modernos, onde a tecnologia floresce,
    User Stories e Epics, com maestria, enriquecem nossa prece.
    Desenvolvedores e stakeholders, em cenário tão vasto,
    Unem-se nesse teatro, com propósito contrasto.

    As User Stories, pequenas narrativas a relatar,
    Descrevem funcionalidades, de forma a elucidar,
    Para os não técnicos, o caminho a trilhar,
    Com clareza e simplicidade, para todos abraçar.

    As Epics, por outro lado, são histórias grandiosas,
    Projetos complexos, em dimensões majestosas.
    Com visão ampla, revelam o horizonte a seguir,
    Guiando o espetáculo, onde todos podem aplaudir.

    Na peça que se desenha, o palco é o software,
    E a plateia, os stakeholders, desejos a compartilhar.
    User Stories e Epics, no roteiro a desenrolar,
    Facilitam a comunicação, fazendo a luz brilhar.

    Assim, nesse palco moderno, a trama se constrói,
    Desenvolvedores e não técnicos, juntos, com nobreçoí.
    User Stories e Epics, como atores, a atuar,
    Trazem entendimento e sucesso, a cada ato a se realizar.
    ```

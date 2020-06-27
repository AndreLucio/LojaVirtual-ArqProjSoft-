# LojaVirtual-ArqProjSoft-
/*Tarefa para a disciplina de Arquitetura e projeto de Software.
 *
 * André Lucio, Matheus Souza, Italo, Octávio.
 * DESCRIÇÂO DO SISTEMA:
 *
 * Apresentaremos uma proposta de loja virtual em MVC/DAO que explora as melhores 
 * práticas e soluções catalogadas em padrões de projetos ratificados pela Gang
 * of Four: MVC, Factory, Singleton, Strategy, Command e memento.
 *
 * O modelo aceito de "comércio" e seu relacionamento cliente-produto-pedido,
 * juntamente com os operadores lógicos e aritméticos envolvidos na compra,
 * cumprem a exigência da tarefa: explorar design patterns com certas soluções
 * reutilizáveis, facilitando sua exposição conceitual. 
 *
 *
 * Factory: A aplicação utiliza o framework Hibernate 4.3x (padrão JPA 2.1),
 * abstraindo o SQL, atuando como Factory de mapeameto objeto-relacional.
 * Poupando esforço de "converter" objetos em registros e registros em objetos.
 * Utiliza annotations nas classes de Model para geração de entidades de 
 * persistência.
 *
 * Inversão de controle: Utilizamos o conceito nas classes do pacote DAO. 
 *
 * Singleton: Utilizado no atributo EntityManagerFactory na classe DAO Conexao.
 * public synchronized static EntityManager garante uma única instância,
 * e torna-a final.
 *
 * A Classe principal ( MenuView.java ) instaciará o Carrinho de compras na 
 * execução, seguindo também o padrão Singleton, garantido que não haja um outro
 * carrinho. O acesso é permitido através do método que retorna a instância única
 * da classe, ou criará uma nova, caso não tenha sido criada.
 * " !Notificando via system output!"
 *
 *
 * Strategy: É utilizada na disponibilização dos algoritmos e operações de 
 * descontos no valor total do pedido, sem necessitar de um switch para cada
 * faixa de desconto.
 *
 * Command: É explorado na associação de cada ação do usuário com o seu respectivo 
 * botão da interface GUI SWING (que nativamente implementa o padrão comportamental.
 * Eles são inicializados usando apenas o objeto "Action". Nos poupando de 
 * "reinventarmos a roda".
 * 
 *
 * Memento: É utilizado na restauração ao estado inicial do carrinho de compras,
 * após anular alguma operação e na do produto selecionado dentro do carrinho.
 * Utilizando os três elementos: Originador, Armazenador e o Memento
 * 
 *
 * Consequentemente, o projeto utiliza outros padrões de projetos não exigidos no
 * escopo da tarefa. Por serem padrões arquiteturais "de praxe" em e-commerce.
 * Contudo, não há necessidade de pormenoriza-los.
 * 
 *
 * MenuView.java assume papel de classe principal (SHIFT + F6)...
 * Operações de banco com HQL são bem mais complexas do que SQL default.
 *
 * É necessário importar a bibliotaca jandex do hibernate para correção:
 * org.jboss.jandex.indexview (download do arquivo jandex/jandex-1.1.0.final.jar)
 * E importar o driver.
 *
 */

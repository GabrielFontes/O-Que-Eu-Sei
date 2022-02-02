# Historinha do rei - Sistema Operacional

Era uma vez um **rei** detentor de um grande lote. Esse rei tinha 5 amigos que precisavam de um lugar para morar. Visto a necessidade, o rei os convidou para que cada um construísse uma casa no lote e foi o que aconteceu.

No espaço que sobrou, o rei plantou uma **horta** para alimentar os amigos e decretou que só poderia entrar uma pessoa por vez na horta. Foi aí que surgiu o primeiro problema. Tinha um dos amigos que estava pegando muitas hortaliças e não estava deixando nada para os outros. Vendo isso, o rei, muito inteligente, interveio:

"A partir de hoje, cada casa terá um tempo para ficar na horta e vou criar uma fila sempre que mais de uma pessoa queira entrar ao mesmo tempo e colocarei um fiscal chamado **KERNEL**!"

Sendo assim, cada pessoa na fila iria receber uma pulseira:

- Novo;
- Pronto;
- Executando;
- Bloqueado;
- Encerrado.

Quando uma pessoa chegava na fila, ela recebia a pulseira "Novo". Quando ela já estava com todas as ferramentas que achava necessário, recebia a pulseira "Pronto", quando ia entrar na horta recebia "Executando". Caso faltasse alguma ferramenta, ele recebia a pulseira "Bloqueado" e ficava na fila até que a ferramenta chegasse. Assim que se encerrava a colheita, a pulseira recebida era a "Encerrado". Isso resolveu parcialmente o problema porque ainda existia um tempo de atraso enquanto uma pessoa saia e a outra entrava.

Um dos amigos, muito inteligente pensou "Se o tempo na horta é por casa, vou chamar 4 pessoas da minha casa para entrar na fila e colher comigo." Deu certo porque agora a casa teria mais tempo na horta. Todavia, começou a sobrar muito alface na casa porque todo mundo pegava muita alface. O outro amigo, criou dois braços mecânicos para ajudá-lo a colher e funcionou. Quanto aos outros 3, um deles conseguiu sobreviver pois comia pouco e os outros 2 não se adaptaram e morreram.

Visto que o problema na horta tinha sido resolvido, o rei decidiu criar uma lei que ajudaria na organização do lote. Para o primeiro amigo, o rei pegou um pedaço limitado do lote e falou: "Pode guardar suas coisas onde quiser dentro do se espaço." Para o segundo amigo, o rei falou: "Cada espaço do seu terreno, vai ser usado para usar um tipo de material e eles se relacionarão para que eu possa fiscalizá-los" Para o terceiro amigo: "Pode usar o espaço que quiser"

E dessa forma, os problemas do rei foram resolvidos e os 3 amigos sobreviventes vivem em constate harmonia.


**Analogia**:

- **Rei** = Sistema Operacional
- **5 amigos** = Programas
- **Horta** = Recurso compartilhado
- **Fiscalizador da horta** = Kernel
- **Amigo que levou a família** = Programa com vários processos
- **Amigo que fez o braço mecânico** = Programa com várias threads
- **Divisão do lote** = Gerenciamento de Arquivos
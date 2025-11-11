# estudos-em-umbanda
Site hospedado com fins de compilar e registrar estudos e leituras sobre temas relacionados a religiosidade afro brasileira, umbanda e espiritualidade. O site será atualizado conforme minhas leituras sobre o tema também avançarem.

Padronização aplicadas nos HTMLs

Resumo das mudanças:
- CSS unificado (baseado em `01 - Fundamentos.html`) e aplicado em: `02`, `03`, `04`.
- Inserido `<h1>` em todas as páginas para consistência visual e SEO.
- Padronizado o placeholder: ícone de bússola + texto "Selecione um tópico no menu para iniciar sua jornada de conhecimento.".
- Alinhado as disclaimers para serem consistentes entre os documentos.
- Adicionado auto-carregamento do primeiro item da barra lateral em `01` (para manter mesmo comportamento entre páginas).
- Criado documento `05 - Observacoes - Lacunas e Sugestoes.md` com lacunas e prioridades de conteúdo faltante, incluindo temas práticos: Defumações, Banhos, Ervas (herbário), Ofertas, Segurança na manipulação de pólvora e enxofre, Pontos Riscados e Cantados, Tronqueira, Bori, Amaci.
 - Criado `content.js` e `00 - Compilado.html` para agregar todo o conteúdo e criar uma versão unificada com barra lateral agrupada e menu colapsável.

- Conteúdo adicionado ao `content.js` (Guia de Estudos Umbandista):
	- `defumacoes` — Defumações (Etùtu): resinas, procedimentos e segurança.
	- `banhos_amaci` — Banhos (Amaci): classificação de ervas, preparos e etiquetas.
	- `herbario_basico` — Herbário Básico Expandido: fichas técnicas de ervas.
	- `oferendas_praticas` — Oferendas práticas (Esquerda & Direita): receitas, locais e descarte.
	- `seguranca_elementos_perigosos` — Segurança com Pólvora, Enxofre, Álcool: protocolos de risco.
	- `bibliografia_comentada` — Bibliografia recomendada por tema.
	- `glossario_expandido` — Glossário expandido de termos críticos.
	- `faq` — Perguntas frequentes (FAQ).

Sugestões de próximos passos (opcionais):
- Criar um `assets/style.css` para centralizar o estilo; deve ser referenciado por todas as páginas.
- Expandir o conteúdo prático: fichas de ervas, receitas com corredicas, pontos de risco e canto com notação musical e imagens de pontos riscados (desenhos vetoriais/PNGs).
- Incluir uma seção de como firmar a Tronqueira e de descarte responsable de oferendas.
- Adicionar bibliografia por capítulo/página para referência direta (ex: Corral p. 37 sobre pontos riscados).
 - Observações sobre `content.js` & `00 - Compilado.html`:
	- O arquivo `content.js` é o repositório principal de conteúdo: cada item é um objeto { id, nome, group, titulo, conteudo, aprofundar }.
	- O arquivo `content.js` é o repositório principal de conteúdo: cada item é um objeto { id, nome, group, titulo, conteudo, aprofundar }.
	- Para editar conteúdo, prefira atualizar `content.js` (use backticks para a propriedade `conteudo` e verifique que não haja backticks não-escapados no HTML interno).
	- Novo campo (opcional): `source` — útil para indicar a origem do conteúdo (ex: "Guia de Estudos Umbandista", "01 - Fundamentos.html"). O campo aparece no `00 - Compilado.html` quando definido.
	 - Novo campo (opcional): `source` — útil para indicar a origem do conteúdo (ex: "Guia de Estudos Umbandista", "01 - Fundamentos.html"). O campo aparece no `00 - Compilado.html` quando definido.
	 - Novo campo (opcional): `tags` — array de strings para pesquisa e categorização (ex: ["defumação","segurança"]).
	 - Novo campo (opcional): `verified` — boolean, indica que o conteúdo foi verificado por referências bibliográficas e assistência editorial.
	 - Novo campo (opcional): `warning` — boolean, indica conteúdo perigoso/gated; `00 - Compilado.html` mostrará um banner e exigirá confirmação do leitor para exibir o conteúdo.
	- `00 - Compilado.html` carrega `content.js` e monta a barra lateral agrupando por `group`. A busca (input) filtra as categorias por texto.
	- Ao adicionar novas categorias, garanta `id` único e atualize `group` para a seção correta. Evite duplicações de id.
	- Para reduzir o tamanho do arquivo compilado no futuro, o conteúdo poderia ser externalizado para arquivos MD e renderizado em tempo de build.

Como revisar localmente:
- Abrir cada HTML no navegador (duplo clique) e confirmar as mudanças visuais.
- Revisar a consistência das `categoriasData` em cada arquivo; onde existirem divergências de conteúdo, alinhar os `id` e `nome` com os temas pretendidos.

Se quiser, eu posso:
- Refatorar os scripts JS para usar um único script compartilhado.
- Transformar esse projeto em um site estático com navegação entre páginas e um CSS centralizado.

Novas adições (Nov 2025):
- Seção "Pesquisa Aprofundada: Etnografia, Matrizes e Simbologia" com navegação interna (#pesq-sec-1 .. #pesq-sec-7), tabelas padronizadas (`table.datatable`) e referências em estilo ABNT.
- Mini-âncoras adicionadas às entradas "Goécia/Teurgia vs Umbanda", "Ética Umbandista" e "Responsabilidade do Médium" para facilitar deep-linking e consulta segmentada.
- Padronização de avisos sensíveis: substituído texto "SACERDOTE ONLY" por "CAUTELA:" mantendo semântica de restrição e supervisão.
- Implementado CSS global para `.internal-nav` e `table.datatable` diretamente em `00 - Compilado.html`.
- Expansão de tags na pesquisa etnográfica para melhorar relevância da busca (itans, ritmos, pontos riscados/cantados, entidades da Esquerda, matrizes culturais).

Como usar as âncoras internas:
- Clicar nos links da caixa "Navegação interna" abre a subseção sem recarregar página.
- É possível referenciar diretamente uma subseção adicionando `#etica-sec-2` (exemplo) ao final da URL.

Boas práticas ao adicionar novas seções:
- Incluir bloco `.internal-nav` quando a entrada exceder ~8 cabeçalhos ou possuir múltiplas dimensões temáticas.
- Garantir IDs únicos em headings (`id="nova-sec-1"` etc.) para evitar colisões de hash.
- Usar `table.datatable` para qualquer tabela — mantém legibilidade e acessibilidade.

Axé!

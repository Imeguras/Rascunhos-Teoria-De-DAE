### Lazy Load

é feito para guardar mémoria, e ser eficiente a retroceder entidades, e para nao carregar informação caso não se saiba se vão ser precisas, as relações permanecem vazias até quando são necessáriass

O entity manager e responsavel por fazer o lazy loading, este processo e extremamente optimizado, ele basicamente tem uma cache, e faz management conforme a memoria que tem available.

Enquanto as entidades estão virtualizadas em vês de ter as entidades no objeto temos proxies.

No ghost basta carregar um parte e ele carrega tudo e põe enabled

quando se uza 

- lazy initialyzation
- ghost(se tocares em um tudo carrega)
- virtual proxy
- virtual holder

Virtual proxy- Enquanto as entidades estão virtualizadas em vês de ter as entidades no objeto temos proxies.

ghost e melhor quando se for preciso um prob vamos precisar de 90% da informação

Virtual holding- e quando se tem varios loadings sucessivos. Da jeito quando cada objeto/linha e mesmo muito pesado

Um Indentity map e basicamente uma hashmap e bom para ler scenas que raramente mudam mas que são lidos frequentementes

# PIPEq-21745 - Preconceito e Discriminação Utilizando Word Embeddings para Quantificar a Evolução Histórica dos Estereótipos Da Discriminação Racial e Embasar Políticas Públicas

### Resumo

A mídia desempenha um papel preponderante na formação e reforço de estereótipos raciais. É crucial combater esses estereótipos, uma vez que podem perpetuar informações incorretas e levar a discriminação, exclusão e outros comportamentos indesejados. Os métodos convencionais de análise de preconceitos e identificação de estereótipos, principalmente em abordagens qualitativas, são limitados quando se trata de grandes volumes de textos devido ao intenso esforço manual necessário. Métodos desenvolvidos para outros idiomas muitas vezes se adaptam ao contexto linguístico e cultural brasileiro. Este artigo apresenta um método baseado em "word embeddings" para analisar estereótipos raciais em artigos jornalísticos em português. Nosso método busca reduzir a ambiguidade de "branco" e "negro" ao se referir a raça, enquanto propomos indicadores alinhados com o contexto brasileiro. A implementação desse método oferece insights sobre a representação racial na mídia brasileira, abrindo caminho para uma representação midiática mais justa e informada ao destacar e compreender esses estereótipos.

### Requisitos

- Python 3.x
- Gensim

### Instalação

Para instalar as dependências necessárias, você pode usar o pip:

```bash
pip install gensim
```

### Exemplo de Uso

Para utilizar o modelo, você pode fazer da seguinte forma:

```python
from gensim.models import Word2Vec

# Carregando o modelo
model = Word2Vec.load('zmb_w2v_1.0')

# Buscar as palavras mais similares a 'negro'
similar_words = model.wv.most_similar('negro', topn=20)

# Imprimir as palavras similares
for word, similarity in similar_words:
    print(f"{word}: {similarity}")
```

### Contribuições

Sinta-se à vontade para contribuir com o projeto, seja adicionando novas funcionalidades, corrigindo bugs ou melhorando a documentação.

### Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.

### Contato

Para mais informações, entre em contato através do email: [silvajo@pucsp.br](mailto:silvajo@pucsp.br)

### Publicações Relacionadas

Para mais informações sobre a pesquisa que deu origem a esse modelo, consulte o artigo completo [aqui](link_para_o_artigo).


![Captura de tela de 2025-01-12 16-50-13](https://github.com/user-attachments/assets/7cb99aec-c2e7-434b-b407-dfc5c5e75a7e)














# Pokédex Project

Este é um projeto de uma Pokédex interativa criada utilizando JavaScript e a API [PokeAPI](https://pokeapi.co/). O objetivo deste projeto é oferecer uma experiência simples e intuitiva para explorar informações sobre Pokémon, incluindo suas características, habilidades e tipos.

## Funcionalidades

- **Busca de Pokémon:** Permite ao usuário pesquisar um Pokémon pelo nome ou ID.
- **Exibição de Informações:** Mostra detalhes como nome, imagem, tipos, habilidades e estatísticas.
- **Navegação Simples:** Possibilidade de avançar e retroceder na listagem de Pokémon.

## Tecnologias Utilizadas

- **HTML5** e **CSS3**: Para estruturação e estilização da interface.
- **JavaScript (ES6+)**: Para manipulação de dados e interatividade.
- **Fetch API**: Para consumir dados da API PokeAPI.

## Como Usar

1. Clone este repositório:

   ```bash
   git clone https://github.com/seu-usuario/pokedex.git
   ```

2. Navegue até o diretório do projeto:

   ```bash
   cd pokedex
   ```

3. Abra o arquivo `index.html` em seu navegador.

## Exemplo de Código

Aqui está um exemplo de como os dados são buscados da PokeAPI:

```javascript
const getPokemon = async (id) => {
  const response = await fetch(`https://pokeapi.co/api/v2/pokemon/${id}`);
  if (!response.ok) {
    throw new Error('Erro ao buscar dados do Pokémon');
  }
  const data = await response.json();
  return data;
};

getPokemon(1)
  .then((pokemon) => console.log(pokemon))
  .catch((error) => console.error(error));
```

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma [issue](https://github.com/seu-usuario/pokedex/issues) ou enviar um pull request.

## Licença

Este projeto está licenciado sob a Licença MIT. Consulte o arquivo `LICENSE` para mais informações.

---

### Próximos Passos

- Implementar funcionalidade de filtro por tipo de Pokémon.
- Adicionar paginação para navegar por mais Pokémon.
- Melhorar a acessibilidade da interface.

```md
# MongoDB - Aula 02 - Exercício
autor: Ramon Barros

## Listagem das databases (passo 2)
rbarros:~/workspace (master) $ mongo be-mean-pokemons
MongoDB shell version: 2.6.11
connecting to: be-mean-pokemons

## Listagem das coleções (passo 3)
> show dbs
admin              (empty)
be-mean-instagram  0.078GB
local              0.078GB

## Cadastro dos pokemons (passo 4)
var pokemon = { name: 'Blastoise', description: 'Ele pode dispara balas de águas com precisão.', attack: 85, defense: 105 }
db.pokemons.insert(pokemon);

var pokemon = { name: 'Pidgey', description: 'Essa sabe onde fica o Alegrete', attack: 35, defense: 35 }
db.pokemons.insert(pokemon);

var pokemon = { name: 'Sandslash', description: 'Um rato com espinhos pontiagudos', attack: 45 , defense: 55 }
db.pokemons.insert(pokemon);

## Lista dos pokemons (passo 5)
db.pokemons.find();

## Busca de pokemon (passo 6)
var query = { name: 'Sandslash' }
var pokemon = db.pokemon.findOne(query);
pokemon


## Atualização do pokemon (passo 6)
pokemon.description = 'Um rato cheio de espinhos';
db.pokemons.save(pokemon);
db.pokemons.find(query)
```

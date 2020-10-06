```attacks.py```

- Why import seed when not used?
- ```python
	def updateAttack(self, newLevel, newRecoil=0, newHeal=0, baseDamage=-1):
        self.pLevel = newLevel
        self.recoil = - (newRecoil*self.pLevel + self.recoil)
        self.heal = newHeal*self.pLevel + self.heal
        self.maxcount = self.maxcount + min(2, max(0, randint(0, 1)), randint(0, 1))
        self.count = self.maxcount
        self.damage = self.calcDamage(baseDamage)
        ```

    + Why newLevel?
    + Why use self.pLevel when already defined?
    + newRecoil and newHeal = 0 deliberately?
    + min(2, max(0, randint(0, 1)), randint(0, 1)) gives 0 or 1 only, replace it with randint(0, 1) 

- baseDamage = -1, why?
- count and maxcount (will probably be explained by another file)


```attacklist.py```

```pokeworld.py```

- Why deepcopy?
- Why [::-1]?


```player.py```

- nonzerohp??
- ```python
for index, pokemon in enumerate(self.archivePokemons):
                pprint(index+1, end=') ')
```

```end-') '```??

- archiveExchange doesn't have any "Press Enter to Continue" or input statement, how does it still work to end the function?
- ```pprint(f"Current Pokemon:")``` : why is f needed when no formatting is there?

- ```python
indexOfCurrent = self.pokemonInHand.index(self.currentPokemon)
            if indexOfCurrent == self.pokemonLimit - 1: return False            
            self.currentPokemon = self.pokemonInHand[(indexOfCurrent+1)%len(self.pokemonInHand)]
            if self.currentPokemon.health <= 0: return False
            pprint(f"{self.name} Chose {self.currentPokemon.name}"); sleep(0.1)
            return True   
```

What is this for? To choose Gary's pokemon? How does it work?

- Return False/True: purpose?
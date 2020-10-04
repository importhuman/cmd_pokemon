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
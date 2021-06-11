class Enemy:
  name = ""
  lives = 0
  def _init_(self, name, lives):
    self.name = name
    self.lives = lives

  def hit(self):
    self.lives -= 1
    if self.lives <= 0:
       print(self.name + ' killed')
    else:
        print(self.name + ' has '+ str(self.lives) + ' lives')

class Monster(Enemy ):
  def _init_(self):
    super()._init_('Monster', 3)

class Alien(Enemy):
  def _init_(self):
    super()._init_('Alien', 5)


m = Monster()
a = Alien()

while True:
    x = input()
    if x == 'exit':
        break
    if x == 'gun':
        m.hit()
    
    if x == 'laser':
        a.hit()

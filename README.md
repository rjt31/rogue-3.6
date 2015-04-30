# rogue-3.6
object oriented final assignment

Tenative file assignment:
// 34 files

	abdul
armor.c
daemon.c
daemons.c
fight.c
weapons.c
rings.c

	jeff
init.c
io.c
list.c
mdport.c
misc.c
vers.c

	tyler
monsters.c
move.c
newlevel.c
pack.c
potions.c
scrolls.c


	scott
options.c
save.c
state.c
sticks.c
xcrpyt.c
rip.c

	ryan
passages.c
rooms.c
things.c
wizard.c
command.c
chase.c
	
	everyone
rogue.h 
rogue.r
main.c
machdep.h

=============== CLASSES =============
class Monster
-wander() // monsters move aimlessly
-runto() // monsters run towards player/gold
-chase() //monster follows player
-remove_mon() // removes monster from room
-genocide() // kills all monsters of given type

class World
struct room	
-walls, stairs, light(), 
createlevel(), newlevel();
placeObjects() //places relevant objects in new level

class Equipment
-armor, weapons, rings, potions, scrolls, gold
-missile(y,x), do_motion(), 
-fall(), init_weapon(), hit_monster() // projectile 
-staves : fix_stick(), do_zap(), charge_str()
-ringon(), ringoff()
-gethand(), ringeat(), ringnum()

class Avatar // may be a variant of the monster class
-move() 
-command() // quaf potions, eat food, etc
-attack() // choosing not to flee, and challenge monster
-hit() // confirms hit, calculates damage
-miss() // hit misses
-thunk() // projectile hitting a monster
-bounce() // projectile missing a monster
-killed() // terminates monster , calls remove_mon()
-wield() // equip a weapon
-quaff() // drink potion
-read_scroll() // activates scroll

class Interface
-menu, dialogue box, inventory
-death(), score(), total_winner(), killname()
-struct inventory, add_pack(), pick_up(), picky_inven(), get_item(), pack_char()


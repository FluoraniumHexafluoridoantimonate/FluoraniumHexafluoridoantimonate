**//this is some code in Gamemaker Studios you should add to add,draw and acction health bar(WARNNING: you must add to an object for it's works!)//
//Create event//**
//instance variables
hp=200
maxhp=200
**//Colison event//**
effect_create_below(ef_firework,x,y,80,c_red)
hp=hp-1
if hp<=0 {
instance_destroy()
effect_create_below(ef_explosion,x,y,80,c_red)
}
with other{
instance_destroy()
}
**//end//**
**//Helth bar on Draw Event//**
draw_sprite(sprite12,-1,x,y)

var barWidth
barWidth=100
draw_set_color(c_red)
draw_rectangle(x,y+20, x+(hp/maxhp)*barWidth, y+20+6,false)
draw_set_color(c_yellow)
draw_rectangle(x,y+20, x+barWidth, y+20+6,true)
**//end//**

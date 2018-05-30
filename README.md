# OpenScad

## Figures  
Hexagon == cylinder(r=10, h=10, $fn=6);
Polygon == cylinder(r=10, h=10, $fn=n);
Cube([x,y,z]);  
cylinder([r=10, h=10]);  --> cylinder(r=10, h=10, $fn=100); fn100 number of polygons    
cono truncada == cylinder(r1=,r2=,h=,$fn=);  
cono == cylinder(r1=,r2=0,h=,$fn=);  
piramide de base hexagonal == == cylinder(r1=,r2=,h=,$fn=6);  
piramide base cuadrada == cylinder(r1=,r2=0,h=,$fn=4);  
tetahedro == cylinder(r1=,r2=0,h=,$fn=3);  


## Movements

rotate([xº,yº,zº]) always from de center  
centre([x,y,z]) 
translate([x,y,z])  

## Taladros    

diference(){  
object to maintain  
object to rest  
}
## Union  

union(){  
object to maintain  
object to rest  
}

## Parameters  
radio=2;  
high=5;  
cylinder(r=radio,h=high);  

## Modules  
module rueda_simple (radio,grosor, radio_eje){  
	difference()  
{	cylinder(r=radio_grande,h=grosor,$fn=100);  
				cylinder(r=radio_eje,h=10,$fn=100,center=true);  
}  
rueda simple(radio=2,grosor=3, radio_eje=7);

### Parameter default  

module rueda_simple (radio=20,grosor=30, radio_eje=2){}  

rueda_simple();  -->radio=20,grosor=30, radio_eje=2  

## Mirror  
mirror([0,1,0]){ object  

## Taladros drill   
i=*x*  
n=*y*  
for(i=[1:n-1]){  
translate([*i*x,y,z])  
cylindre(r=3,h=4,$fn=300,centre=true)  
}    
  
## Color   
color(* red *,0,5)  *0,5 es la transparencia*  
! solo aparece el objet0
* no aparece este objeto
% tranparece

## Redondear  
--> utiliza las tangentes  
hull(){}  

## Minkowski  
minlowski(){  
pieza  
cylinder (just horizontal edge) or sphere (horizontal and vertical edges)  
}  
## Figures 2D  
triangel == circle(d=10, $fn=3);  
square == square(length, height);  
5,6,7.. circle(d=10, $fn=n);  
circle==circle(d=10, $fn=100);  
### Figures 2D to 3D  
linear_extrude(height=*X*,center=)  
polygon([points,points...]);  
twist  -->linear_extrude(height=*X*,twist= º,center=)  




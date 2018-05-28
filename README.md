# OpenScad

## Figures  
Hexagon == cylinder(r=10, h=10, $fn=6);
Polygon == cylinder(r=10, h=10, $fn=n);
Cube([x,y,z]);  
cylinder([r=10, h=10]);  --> cylinder(r=10, h=10, $fn=100); fn100 number of polygons    

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

##Taladros drill   
i=*x*  
n=*y*  
for(i=[1:n-1]){  
translate([*i*x,y,z])  
cylindre(r=3,h=4,$fn=300,centre=true)  
}    
  
## Color   
color(* red *)  
! solo aparece el objet0
* no aparece este objeto

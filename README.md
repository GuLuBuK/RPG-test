# RPG-test
Un test pour un rpg tour a tour
<script>

// PV veut dire Points de Vie
var PV = 12;

function attaque() {
	
    if(PV <= 0){
        alert("Sans et papyrus sont morts ! :-)");
    }
    else {
    	var degats = getRandomMinMax (2, 4);
        PV = PV-degats;
        if (PV > 0) {
        	alert("Sans et papyrus ont perdu "+degats+" PV. Il leur en reste "+PV);
        }
    }
}

function soigne() {
	
    if(PV <= 0){
        alert("Sans et papyrus sont est déjà mort ! On ne peut pas les soigner !")
    }
	else if(PV >= 12){
        alert("Sans et Papyrus ont points de vie déjà au maximum.");
    }
    else {
       	var soins = getRandomMinMax (1, 3);
        PV = PV+soins;
        if(PV > 12){
        	PV = 12;
       	}
        
        if(PV > 0){       
        	alert("Sans et papyrus ont gagné "+soins+" PV. Ils en ont maintenant "+PV);
       	}
    }
}

function getRandomMinMax (min, max){
	return Math.floor (Math.random()*(max-min)) +min
}





</script>
<button onclick="attaque()">Get dunked on !</button>
<button onclick="soigne()">Mercy</button>
<img src ="http://cloud-3.steamusercontent.com/ugc/385414506607854008/34907E3CC4D849030041EBBFE45DF236681EDC2D/" />

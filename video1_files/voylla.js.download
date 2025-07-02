var logo = document.createElement("IMG");

logo.src = "https://whatsapp-widget.s3.ap-south-1.amazonaws.com/wa-logo-120.png";

logo.width = "60";

logo.height = "60";

var a = document.createElement('a');

a.appendChild(logo);

a.title = "Chat with us on WhatsApp";

a.href = "https://wa.me/+917230066751?text=";

a.style.zIndex = 100000000;

a.style.position = "fixed";

a.style.bottom = "0px";

a.style.right = "0px";

a.style.padding = "10px";

var clientName = "voylla"

document.body.appendChild(a);

a.target="_blank"

a.onclick = (()=>{

    updateCount('WHATSAPP_REDIRECTION')

})

function updateCount(eventName){



            var newPrimaryHashKey = "obj_name:" + generateRowId(4);

            const payload = {

                id: clientName + newPrimaryHashKey,

                clientName: clientName,

                dateTime: new Date().toUTCString(),

                eventName: eventName

            }

            fetch('https://n7ze0y2wwa.execute-api.ap-south-1.amazonaws.com/default/', {

                  method: "POST",

                      headers: {

      'Accept': 'application/json',

      'Content-Type': 'application/json'

    },

                  body: JSON.stringify(payload)

            }).then(data=> data.json()).then(data=>{

            }).catch((error)=>{

            })

}

        

function generateRowId(shardId /* range 0-64 for shard/slot */) {

            var CUSTOMEPOCH = 1300000000000; 

            var ts = new Date().getTime() - CUSTOMEPOCH; // limit to recent

            var randid = Math.floor(Math.random() * 512);

            ts = (ts * 64);   // bit-shift << 6

            ts = ts + shardId;

            return (ts * 512) + randid;

}
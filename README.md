# VenuzBotSupport
<h1 align="center"><img src="https://cdn.discordapp.com/attachments/737775780226007112/862019248406396938/Icon_Venuz_1.0.png" width="30px"> Venuz Bot <img src="https://cdn.discordapp.com/attachments/737775780226007112/862019248406396938/Icon_Venuz_1.0.png" width="30px"></h1>
<p align="center">Gracias por la ayuda!</p>

- Repositorio de Venuz bot en Discord y Telegram.

## ✨Latest Updates✨

> Sistema de suscripción VIP por invitaciones.
> Sistema de invitaciones
> Página web

## ✨Announce✨

- Este proyecto pertenece al grupo *Dev's Lounge* Administrado por Venuz#1670 - OWNER




- Por la ayuda brindada dejaré algunas plantillas para otras `redes sociales`. Si gustás ayuda en los códigos dejados aquí únete a nuestro servidor de Discord.
## Messenger

> The rest of the code implements the routes for our Express server.
 
    let app = express();

    app.use(bodyParser.json());
    app.use(bodyParser.urlencoded({
    extended: true
    }));
 
> Webhook validation

         app.get('/webhook', function(req, res) {
         if (req.query['hub.mode'] === 'subscribe' &&
         req.query['hub.verify_token'] === process.env.VERIFY_TOKEN) {
         console.log("Validating webhook");
         res.status(200).send(req.query['hub.challenge']);
           } else {
           console.error("Failed validation. Make sure the validation tokens match.");
         res.sendStatus(403);          
         }
         });

> Display the web page

            app.get('/', function(req, res) {
            res.writeHead(200, {'Content-Type': 'text/html'});
            res.write(messengerButton);
            res.end();
            });

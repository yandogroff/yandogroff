async function enviarScript(scriptText){
	const lines = scriptText.split(/[\n\t]+/).map(line => line.trim()).filter(line => line);
	main = document.querySelector("#main"),
	textarea = main.querySelector(`div[contenteditable="true"]`)
	
	if(!textarea) throw new Error("Não há uma conversa aberta")
	
	for(const line of lines){
		console.log(line)
	
		textarea.focus();
		document.execCommand('insertText', false, line);
		textarea.dispatchEvent(new Event('change', {bubbles: true}));
	
		setTimeout(() => {
			(main.querySelector(`[data-testid="send"]`) || main.querySelector(`[data-icon="send"]`)).click();
		}, 100);
		
		if(lines.indexOf(line) !== lines.length - 1) await new Promise(resolve => setTimeout(resolve, 250));
	}
	
	return lines.length;
}

enviarScript(`
We could leave the Christmas lights up 'til January
This is our place, we make the rules
And there's a dazzling haze
A mysterious way about you dear
Have I known you 20 seconds or 20 years?

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
You're my, my, my, my lover

We could let our friends crash in the living room
This is our place, we make the call
And I'm highly suspicious
that everyone who sees you wants you
I've loved you three summers now, honey
But I want 'em all

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my lover

Ladies and gentlemen, will you please stand?
With every guitar string scar on my hand
I take this magnetic force of a man to be my lover
My heart's been borrowed and yours has been blue
All's well that ends well to end up with you
Swear to be overdramatic and true to my lover
And you'll save all your dirtiest jokes for me
And at every table, I'll save you a seat, lover

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my
Oh, you're my, my, my, my
Darling, you're my, my, my, my lover
We could leave the Christmas lights up 'til January
This is our place, we make the rules
And there's a dazzling haze
A mysterious way about you dear
Have I known you 20 seconds or 20 years?

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
You're my, my, my, my lover

We could let our friends crash in the living room
This is our place, we make the call
And I'm highly suspicious
that everyone who sees you wants you
I've loved you three summers now, honey
But I want 'em all

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my lover

Ladies and gentlemen, will you please stand?
With every guitar string scar on my hand
I take this magnetic force of a man to be my lover
My heart's been borrowed and yours has been blue
All's well that ends well to end up with you
Swear to be overdramatic and true to my lover
And you'll save all your dirtiest jokes for me
And at every table, I'll save you a seat, lover

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my
Oh, you're my, my, my, my
Darling, you're my, my, my, my lover
We could leave the Christmas lights up 'til January
This is our place, we make the rules
And there's a dazzling haze
A mysterious way about you dear
Have I known you 20 seconds or 20 years?

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
You're my, my, my, my lover

We could let our friends crash in the living room
This is our place, we make the call
And I'm highly suspicious
that everyone who sees you wants you
I've loved you three summers now, honey
But I want 'em all

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my lover

Ladies and gentlemen, will you please stand?
With every guitar string scar on my hand
I take this magnetic force of a man to be my lover
My heart's been borrowed and yours has been blue
All's well that ends well to end up with you
Swear to be overdramatic and true to my lover
And you'll save all your dirtiest jokes for me
And at every table, I'll save you a seat, lover

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my
Oh, you're my, my, my, my
Darling, you're my, my, my, my lover
We could leave the Christmas lights up 'til January
This is our place, we make the rules
And there's a dazzling haze
A mysterious way about you dear
Have I known you 20 seconds or 20 years?

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
You're my, my, my, my lover

We could let our friends crash in the living room
This is our place, we make the call
And I'm highly suspicious
that everyone who sees you wants you
I've loved you three summers now, honey
But I want 'em all

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my lover

Ladies and gentlemen, will you please stand?
With every guitar string scar on my hand
I take this magnetic force of a man to be my lover
My heart's been borrowed and yours has been blue
All's well that ends well to end up with you
Swear to be overdramatic and true to my lover
And you'll save all your dirtiest jokes for me
And at every table, I'll save you a seat, lover

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my
Oh, you're my, my, my, my
Darling, you're my, my, my, my lover
Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti

Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti
Me diga agora por favor
Que eu vou correndo te abraçar
Te quero tanto, é quase dor
É com você que eu quero estar

Se for por mim
Vai ser assim
É só você querer

Pra gente, enfim, se amar
Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti

Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti
Me diga agora por favor
Que eu vou correndo te abraçar
Te quero tanto, é quase dor
É com você que eu quero estar

Se for por mim
Vai ser assim
É só você querer

Pra gente, enfim, se amar
Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti

Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti
Me diga agora por favor
Que eu vou correndo te abraçar
Te quero tanto, é quase dor
É com você que eu quero estar

Se for por mim
Vai ser assim
É só você querer

Pra gente, enfim, se amar
Eu poderia acordar sem teu olhar de sono
Sem teu lábio que é dono
Mas eu não quero
Eu não quero

Eu poderia encantar qualquer outro par de ouvidos
Não te ter mais aqui comigo
Mas eu não quero não
Eu não quero

Poderia imaginar
Ou até acostumar
O meu querer noutro lugar
Tanta coisa em que aqui cabe um sim
Mas não

Porque eu te amo
E não consigo me ver sem ser o teu amor por anos
Não é acaso, é só amor
Não existe engano
Que me carregue pra longe
E que te faça outros planos, meu bem
Teu cheiro só tu tem
Tua boca só tu tem
Me tem

Eu poderia não viver tuas primeiras rugas
Nem estar aqui pra adivinhar a tua memória em fuga
Mas eu não quero
Eu não quero
Eu poderia não lidar
Eu poderia nem ligar
Mas não, não, não
Eu não quero não
Poderia imaginar
Ou até acostumar
O meu querer noutro lugar
Tanta coisa em que aqui cabe um sim
Mas não

Porque eu te amo
E não consigo me ver sem ser o teu amor por anos
Não é acaso, é só amor
Não existe engano
Que me carregue pra longe
E que te faça outros planos, meu bem
Teu cheiro só tu tem
Tua boca só tu tem

Tanta cara
Tanta esquina
Tanto fogo
Tanta fome
Tanta rima
É tanta coisa que nem sei onde vai dar
Tanto que eu posso imaginar
Tanta falta Tanta fome
Tanta pressa
Tanta, tanta, tanta
Tanta coisa em que aqui cabe um sim, mas não
Eu poderia acordar sem teu olhar de sono
Sem teu lábio que é dono
Mas eu não quero
Eu não quero

Eu poderia encantar qualquer outro par de ouvidos
Não te ter mais aqui comigo
Mas eu não quero não
Eu não quero

Poderia imaginar
Ou até acostumar
O meu querer noutro lugar
Tanta coisa em que aqui cabe um sim
Mas não

Porque eu te amo
E não consigo me ver sem ser o teu amor por anos
Não é acaso, é só amor
Não existe engano
Que me carregue pra longe
E que te faça outros planos, meu bem
Teu cheiro só tu tem
Tua boca só tu tem
Me tem

Eu poderia não viver tuas primeiras rugas
Nem estar aqui pra adivinhar a tua memória em fuga
Mas eu não quero
Eu não quero
Eu poderia não lidar
Eu poderia nem ligar
Mas não, não, não
Eu não quero não
Poderia imaginar
Ou até acostumar
O meu querer noutro lugar
Tanta coisa em que aqui cabe um sim
Mas não

Porque eu te amo
E não consigo me ver sem ser o teu amor por anos
Não é acaso, é só amor
Não existe engano
Que me carregue pra longe
E que te faça outros planos, meu bem
Teu cheiro só tu tem
Tua boca só tu tem

Tanta cara
Tanta esquina
Tanto fogo
Tanta fome
Tanta rima
É tanta coisa que nem sei onde vai dar
Tanto que eu posso imaginar
Tanta falta Tanta fome
Tanta pressa
Tanta, tanta, tanta
Tanta coisa em que aqui cabe um sim, mas não
Ei
Fiz questão da promessa lembrar
Tu jurou minha mão não soltar
E se foi junto dela

Ei
Cê não sabe a falta que faz
Será que teus dias tão iguais?
Eu me pego pensando

Ai, amor
Será que tu divide a dor
Do teu peito cansado
Com alguém que não vai te sarar?
Meu amor
Eu vivo no aguardo
De ver você voltando
Cruzando a porta
Parararara

Ei
Diz pra mim o que eu quero escutar
Só você sabe adivinhar
Meus desejos secretos

Ei
Faz de conta que não percebi
Que você não esteve aqui
Com teu jeito singelo

Sem hora pra voltar
Sem rota pra tua fuga
Com tempo pra perder
Teu olho degradê pra colorir
Pra colorir
Ei
Fiz questão da promessa lembrar
Tu jurou minha mão não soltar
E se foi junto dela

Ei
Cê não sabe a falta que faz
Será que teus dias tão iguais?
Eu me pego pensando

Ai, amor
Será que tu divide a dor
Do teu peito cansado
Com alguém que não vai te sarar?
Meu amor
Eu vivo no aguardo
De ver você voltando
Cruzando a porta
Parararara

Ei
Diz pra mim o que eu quero escutar
Só você sabe adivinhar
Meus desejos secretos

Ei
Faz de conta que não percebi
Que você não esteve aqui
Com teu jeito singelo

Sem hora pra voltar
Sem rota pra tua fuga
Com tempo pra perder
Teu olho degradê pra colorir
Pra colorir
Ei
Fiz questão da promessa lembrar
Tu jurou minha mão não soltar
E se foi junto dela

Ei
Cê não sabe a falta que faz
Será que teus dias tão iguais?
Eu me pego pensando

Ai, amor
Será que tu divide a dor
Do teu peito cansado
Com alguém que não vai te sarar?
Meu amor
Eu vivo no aguardo
De ver você voltando
Cruzando a porta
Parararara

Ei
Diz pra mim o que eu quero escutar
Só você sabe adivinhar
Meus desejos secretos

Ei
Faz de conta que não percebi
Que você não esteve aqui
Com teu jeito singelo

Sem hora pra voltar
Sem rota pra tua fuga
Com tempo pra perder
Teu olho degradê pra colorir
Pra colorir
I walked through the door with you, the air was cold
But something 'bout it felt like home somehow
And I left my scarf there at your sister's house
And you've still got it in your drawer, even now
Oh, your sweet disposition and my wide-eyed gaze
We're singing in the car, getting lost upstate
Autumn leaves falling down like pieces into place
And I can picture it after all these days

And I know it's long gone and
That magic's not here no more
And I might be okay, but I'm not fine at all
Oh, oh, oh

'Cause there we are again on that little town street
You almost ran the red 'cause you were lookin' over at me
Wind in my hair, I was there
I remember it all too well

Photo album on the counter, your cheeks were turning red
You used to be a little kid with glasses in a twin-sized bed
And your mother's telling stories 'bout you on the tee-ball team
You tell me 'bout your past, thinking your future was me
And you were tossing me the car keys, fuck the patriarchy
Key chain on the ground, we were always skipping town
And I was thinking on the drive down, any time now
He's gonna say it's love, you never called it what it was
'Til we were dead and gone and buried
Check the pulse and come back swearing it's the same
After three months in the grave
And then you wondered where it went to as I reached for you
But all I felt was shame and you held my lifeless frame

And I know it's long gone and
There was nothing else I could do
And I forget about you long enough
To forget why I needed to

'Cause there we are again in the middle of the night
We're dancing 'round the kitchen in the refrigerator light
Down the stairs, I was there
I remember it all too well
And there we are again when nobody had to know
You kept me like a secret but I kept you like an oath
Sacred prayer, and we'd swear
To remember it all too well, yeah

Maybe we got lost in translation
Maybe I asked for too much
But maybe this thing was a masterpiece
'Til you tore it all up
Running scared, I was there
I remember it all too well
And you call me up again
Just to break me like a promise
So casually cruel in the name of being honest
I'm a crumpled up piece of paper lying here
'Cause I remember it all, all, all

They say all's well that ends well
But I'm in a new hell every time you double-cross my mind
You said if we had been closer in age
maybe it would have been fine
And that made me want to die
The idea you had of me, who was she?
A never needing ever lovely jewel whose shine reflects on you
Not weeping in a party bathroom
Some actress asking me what happened
you, that's what happened, you
You who charmed my dad with self-effacing jokes
Sipping coffee like you're on a late night show
But then he watched me watch the front door all night, willing you to come
And he said, "It's supposed to be fun turning twenty-one"

Time won't fly, it's like I'm paralyzed by it
I'd like to be my old self again, but I'm still trying to find it
After plaid shirt days and nights when you made me your own
Now you mail back my things and I walk home alone
But you keep my old scarf from that very first week
'Cause it reminds you of innocence and it smells like me
You can't get rid of it
'Cause you remember it all too well, yeah
'Cause there we are again when I loved you so
Back before you lost the one real thing you've ever known

It was rare, I was there
I remember it all too well
Wind in my hair, you were there
You remember it all
Down the stairs, you were there
You remember it all
It was rare, I was there
I remember it all too well

And I was never good at telling jokes but the punch line goes
I'll get older but your lovers stay my age
From when your Brooklyn broke my skin and bones
I'm a soldier who's returning half her weight
And did the twin flame bruise paint you blue?
Just between us, did the love affair maim you too?
Cause in this city's barren cold
I still remember the first fall of snow
And how it glistened as it fell, I remember it all too well

Just between us, did the love affair maim you all too well?
Just between us, do you remember it all too well?
Just between us, I remember it (Just between us) all too well
Wind in my hair, I was there, I was there
Down the stairs, I was there, I was there
Sacred prayer, I was there, I was there
It was rare, you remember it all too well
Wind in my hair, I was there, I was there
Down the stairs, I was there, I was there
Sacred prayer, I was there, I was there
It was rare, you remember it
Wind in my hair, I was there, I was there
Down the stairs, I was there, I was there
Sacred prayer, I was there, I was there
It was rare, you remember it
Wind in my hair, I was there, I was there
Down the stairs, I was there, I was there
Sacred prayer, I was there, I was there
It was rare, you remember it
We could leave the Christmas lights up 'til January
This is our place, we make the rules
And there's a dazzling haze
A mysterious way about you dear
Have I known you 20 seconds or 20 years?

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
You're my, my, my, my lover

We could let our friends crash in the living room
This is our place, we make the call
And I'm highly suspicious
that everyone who sees you wants you
I've loved you three summers now, honey
But I want 'em all

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my lover

Ladies and gentlemen, will you please stand?
With every guitar string scar on my hand
I take this magnetic force of a man to be my lover
My heart's been borrowed and yours has been blue
All's well that ends well to end up with you
Swear to be overdramatic and true to my lover
And you'll save all your dirtiest jokes for me
And at every table, I'll save you a seat, lover

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my
Oh, you're my, my, my, my
Darling, you're my, my, my, my lover
We could leave the Christmas lights up 'til January
This is our place, we make the rules
And there's a dazzling haze
A mysterious way about you dear
Have I known you 20 seconds or 20 years?

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
You're my, my, my, my lover

We could let our friends crash in the living room
This is our place, we make the call
And I'm highly suspicious
that everyone who sees you wants you
I've loved you three summers now, honey
But I want 'em all

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my lover

Ladies and gentlemen, will you please stand?
With every guitar string scar on my hand
I take this magnetic force of a man to be my lover
My heart's been borrowed and yours has been blue
All's well that ends well to end up with you
Swear to be overdramatic and true to my lover
And you'll save all your dirtiest jokes for me
And at every table, I'll save you a seat, lover

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my
Oh, you're my, my, my, my
Darling, you're my, my, my, my lover
We could leave the Christmas lights up 'til January
This is our place, we make the rules
And there's a dazzling haze
A mysterious way about you dear
Have I known you 20 seconds or 20 years?

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
You're my, my, my, my lover

We could let our friends crash in the living room
This is our place, we make the call
And I'm highly suspicious
that everyone who sees you wants you
I've loved you three summers now, honey
But I want 'em all

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my lover

Ladies and gentlemen, will you please stand?
With every guitar string scar on my hand
I take this magnetic force of a man to be my lover
My heart's been borrowed and yours has been blue
All's well that ends well to end up with you
Swear to be overdramatic and true to my lover
And you'll save all your dirtiest jokes for me
And at every table, I'll save you a seat, lover

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my
Oh, you're my, my, my, my
Darling, you're my, my, my, my lover
We could leave the Christmas lights up 'til January
This is our place, we make the rules
And there's a dazzling haze
A mysterious way about you dear
Have I known you 20 seconds or 20 years?

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
You're my, my, my, my lover

We could let our friends crash in the living room
This is our place, we make the call
And I'm highly suspicious
that everyone who sees you wants you
I've loved you three summers now, honey
But I want 'em all

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my lover

Ladies and gentlemen, will you please stand?
With every guitar string scar on my hand
I take this magnetic force of a man to be my lover
My heart's been borrowed and yours has been blue
All's well that ends well to end up with you
Swear to be overdramatic and true to my lover
And you'll save all your dirtiest jokes for me
And at every table, I'll save you a seat, lover

Can I go where you go?
Can we always be this close forever and ever?
And ah, take me out, and take me home
(Forever and ever)
You're my, my, my, my
Oh, you're my, my, my, my
Darling, you're my, my, my, my lover
Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti

Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti
Me diga agora por favor
Que eu vou correndo te abraçar
Te quero tanto, é quase dor
É com você que eu quero estar

Se for por mim
Vai ser assim
É só você querer

Pra gente, enfim, se amar
Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti

Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti
Me diga agora por favor
Que eu vou correndo te abraçar
Te quero tanto, é quase dor
É com você que eu quero estar

Se for por mim
Vai ser assim
É só você querer

Pra gente, enfim, se amar
Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti

Eu vejo tua cara
O teu querer perverso
A gente fica bem aqui no chão da sala
Eu te queria a vida toda
Te confesso
Por mim, a gente nem precisa mais da estrada

Eu vejo você longe
E quero você perto
Fica na minha sombra
Eu posso ser teu rastro
Não quero tu na linha
Vivo, morto ou Claro
Eu quero tu na minha boca
A minha boca quer você

Diga pra mim que é real
Que eu te prometo meu melhor
Fala pra mim o que eu quero ouvir
Que tu sentiu o que eu senti
Me diga agora por favor
Que eu vou correndo te abraçar
Te quero tanto, é quase dor
É com você que eu quero estar

Se for por mim
Vai ser assim
É só você querer

Pra gente, enfim, se amar
Eu poderia acordar sem teu olhar de sono
Sem teu lábio que é dono
Mas eu não quero
Eu não quero

Eu poderia encantar qualquer outro par de ouvidos
Não te ter mais aqui comigo
Mas eu não quero não
Eu não quero

Poderia imaginar
Ou até acostumar
O meu querer noutro lugar
Tanta coisa em que aqui cabe um sim
Mas não

Porque eu te amo
E não consigo me ver sem ser o teu amor por anos
Não é acaso, é só amor
Não existe engano
Que me carregue pra longe
E que te faça outros planos, meu bem
Teu cheiro só tu tem
Tua boca só tu tem
Me tem

Eu poderia não viver tuas primeiras rugas
Nem estar aqui pra adivinhar a tua memória em fuga
Mas eu não quero
Eu não quero
Eu poderia não lidar
Eu poderia nem ligar
Mas não, não, não
Eu não quero não
Poderia imaginar
Ou até acostumar
O meu querer noutro lugar
Tanta coisa em que aqui cabe um sim
Mas não

Porque eu te amo
E não consigo me ver sem ser o teu amor por anos
Não é acaso, é só amor
Não existe engano
Que me carregue pra longe
E que te faça outros planos, meu bem
Teu cheiro só tu tem
Tua boca só tu tem

Tanta cara
Tanta esquina
Tanto fogo
Tanta fome
Tanta rima
É tanta coisa que nem sei onde vai dar
Tanto que eu posso imaginar
Tanta falta Tanta fome
Tanta pressa
Tanta, tanta, tanta
Tanta coisa em que aqui cabe um sim, mas não
Eu poderia acordar sem teu olhar de sono
Sem teu lábio que é dono
Mas eu não quero
Eu não quero

Eu poderia encantar qualquer outro par de ouvidos
Não te ter mais aqui comigo
Mas eu não quero não
Eu não quero

Poderia imaginar
Ou até acostumar
O meu querer noutro lugar
Tanta coisa em que aqui cabe um sim
Mas não

Porque eu te amo
E não consigo me ver sem ser o teu amor por anos
Não é acaso, é só amor
Não existe engano
Que me carregue pra longe
E que te faça outros planos, meu bem
Teu cheiro só tu tem
Tua boca só tu tem
Me tem

Eu poderia não viver tuas primeiras rugas
Nem estar aqui pra adivinhar a tua memória em fuga
Mas eu não quero
Eu não quero
Eu poderia não lidar
Eu poderia nem ligar
Mas não, não, não
Eu não quero não
Poderia imaginar
Ou até acostumar
O meu querer noutro lugar
Tanta coisa em que aqui cabe um sim
Mas não

Porque eu te amo
E não consigo me ver sem ser o teu amor por anos
Não é acaso, é só amor
Não existe engano
Que me carregue pra longe
E que te faça outros planos, meu bem
Teu cheiro só tu tem
Tua boca só tu tem

Tanta cara
Tanta esquina
Tanto fogo
Tanta fome
Tanta rima
É tanta coisa que nem sei onde vai dar
Tanto que eu posso imaginar
Tanta falta Tanta fome
Tanta pressa
Tanta, tanta, tanta
Tanta coisa em que aqui cabe um sim, mas não
Ei
Fiz questão da promessa lembrar
Tu jurou minha mão não soltar
E se foi junto dela

Ei
Cê não sabe a falta que faz
Será que teus dias tão iguais?
Eu me pego pensando

Ai, amor
Será que tu divide a dor
Do teu peito cansado
Com alguém que não vai te sarar?
Meu amor
Eu vivo no aguardo
De ver você voltando
Cruzando a porta
Parararara

Ei
Diz pra mim o que eu quero escutar
Só você sabe adivinhar
Meus desejos secretos

Ei
Faz de conta que não percebi
Que você não esteve aqui
Com teu jeito singelo

Sem hora pra voltar
Sem rota pra tua fuga
Com tempo pra perder
Teu olho degradê pra colorir
Pra colorir
Ei
Fiz questão da promessa lembrar
Tu jurou minha mão não soltar
E se foi junto dela

Ei
Cê não sabe a falta que faz
Será que teus dias tão iguais?
Eu me pego pensando

Ai, amor
Será que tu divide a dor
Do teu peito cansado
Com alguém que não vai te sarar?
Meu amor
Eu vivo no aguardo
De ver você voltando
Cruzando a porta
Parararara

Ei
Diz pra mim o que eu quero escutar
Só você sabe adivinhar
Meus desejos secretos

Ei
Faz de conta que não percebi
Que você não esteve aqui
Com teu jeito singelo

Sem hora pra voltar
Sem rota pra tua fuga
Com tempo pra perder
Teu olho degradê pra colorir
Pra colorir
Ei
Fiz questão da promessa lembrar
Tu jurou minha mão não soltar
E se foi junto dela

Ei
Cê não sabe a falta que faz
Será que teus dias tão iguais?
Eu me pego pensando

Ai, amor
Será que tu divide a dor
Do teu peito cansado
Com alguém que não vai te sarar?
Meu amor
Eu vivo no aguardo
De ver você voltando
Cruzando a porta
Parararara

Ei
Diz pra mim o que eu quero escutar
Só você sabe adivinhar
Meus desejos secretos

Ei
Faz de conta que não percebi
Que você não esteve aqui
Com teu jeito singelo

Sem hora pra voltar
Sem rota pra tua fuga
Com tempo pra perder
Teu olho degradê pra colorir
Pra colorir
I walked through the door with you, the air was cold
But something 'bout it felt like home somehow
And I left my scarf there at your sister's house
And you've still got it in your drawer, even now
Oh, your sweet disposition and my wide-eyed gaze
We're singing in the car, getting lost upstate
Autumn leaves falling down like pieces into place
And I can picture it after all these days

And I know it's long gone and
That magic's not here no more
And I might be okay, but I'm not fine at all
Oh, oh, oh

'Cause there we are again on that little town street
You almost ran the red 'cause you were lookin' over at me
Wind in my hair, I was there
I remember it all too well

Photo album on the counter, your cheeks were turning red
You used to be a little kid with glasses in a twin-sized bed
And your mother's telling stories 'bout you on the tee-ball team
You tell me 'bout your past, thinking your future was me
And you were tossing me the car keys, fuck the patriarchy
Key chain on the ground, we were always skipping town
And I was thinking on the drive down, any time now
He's gonna say it's love, you never called it what it was
'Til we were dead and gone and buried
Check the pulse and come back swearing it's the same
After three months in the grave
And then you wondered where it went to as I reached for you
But all I felt was shame and you held my lifeless frame

And I know it's long gone and
There was nothing else I could do
And I forget about you long enough
To forget why I needed to

'Cause there we are again in the middle of the night
We're dancing 'round the kitchen in the refrigerator light
Down the stairs, I was there
I remember it all too well
And there we are again when nobody had to know
You kept me like a secret but I kept you like an oath
Sacred prayer, and we'd swear
To remember it all too well, yeah

Maybe we got lost in translation
Maybe I asked for too much
But maybe this thing was a masterpiece
'Til you tore it all up
Running scared, I was there
I remember it all too well
And you call me up again
Just to break me like a promise
So casually cruel in the name of being honest
I'm a crumpled up piece of paper lying here
'Cause I remember it all, all, all

They say all's well that ends well
But I'm in a new hell every time you double-cross my mind
You said if we had been closer in age
maybe it would have been fine
And that made me want to die
The idea you had of me, who was she?
A never needing ever lovely jewel whose shine reflects on you
Not weeping in a party bathroom
Some actress asking me what happened
you, that's what happened, you
You who charmed my dad with self-effacing jokes
Sipping coffee like you're on a late night show
But then he watched me watch the front door all night, willing you to come
And he said, "It's supposed to be fun turning twenty-one"

Time won't fly, it's like I'm paralyzed by it
I'd like to be my old self again, but I'm still trying to find it
After plaid shirt days and nights when you made me your own
Now you mail back my things and I walk home alone
But you keep my old scarf from that very first week
'Cause it reminds you of innocence and it smells like me
You can't get rid of it
'Cause you remember it all too well, yeah
'Cause there we are again when I loved you so
Back before you lost the one real thing you've ever known

It was rare, I was there
I remember it all too well
Wind in my hair, you were there
You remember it all
Down the stairs, you were there
You remember it all
It was rare, I was there
I remember it all too well

And I was never good at telling jokes but the punch line goes
I'll get older but your lovers stay my age
From when your Brooklyn broke my skin and bones
I'm a soldier who's returning half her weight
And did the twin flame bruise paint you blue?
Just between us, did the love affair maim you too?
Cause in this city's barren cold
I still remember the first fall of snow
And how it glistened as it fell, I remember it all too well

Just between us, did the love affair maim you all too well?
Just between us, do you remember it all too well?
Just between us, I remember it (Just between us) all too well
Wind in my hair, I was there, I was there
Down the stairs, I was there, I was there
Sacred prayer, I was there, I was there
It was rare, you remember it all too well
Wind in my hair, I was there, I was there
Down the stairs, I was there, I was there
Sacred prayer, I was there, I was there
It was rare, you remember it
Wind in my hair, I was there, I was there
Down the stairs, I was there, I was there
Sacred prayer, I was there, I was there
It was rare, you remember it
Wind in my hair, I was there, I was there
Down the stairs, I was there, I was there
Sacred prayer, I was there, I was there
It was rare, you remember it
Não tenho culpa se teu beijo encaixou tão bem
Se nossos olhos não tem olhos para mais ninguém
Se meia hora depois que a gente se solta sente saudade
Então, por que não dorme aqui?
Minha camisa pode ser o seu pijama
Se preferir cê pode ficar a semana
Porque por mim você nem ia embora
Muda pra minha vida
E vem se apertar comigo na cama de solteiro
Aqui cabe as suas coisas, nosso amor inteiro
Eu não me importo em ceder espaço pra caber nós dois
Muda pra minha vida
E vem se apertar comigo na cama de solteiro
Aqui cabe as suas coisas, nosso amor inteiro
Eu não me importo em ceder espaço pra caber nós dois
E a cama de casal eu arrumo depois
Yara Tchê, Alessando Costa
Somos nós, Seu Desejo (Seu Desejo)
Diz!
Não tenho culpa se teu beijo encaixou tão bem
Se nossos olhos não tem olhos para mais ninguém
Se meia hora depois que a gente se solta
Escuta assim, ó
Então, por que não dorme aqui?
Minha camisa pode ser o seu pijama
Se preferir cê pode ficar a semana
Porque por mim você nem ia embora
Muda pra minha vida
E vem se apertar comigo na cama de solteiro
Aqui cabe as suas coisas, nosso amor inteiro
Eu não me importo em ceder espaço pra caber nós dois
Muda pra minha vida
E vem se apertar comigo na cama de solteiro
Aqui cabe as suas coisas, nosso amor inteiro
Eu não me importo em ceder espaço pra caber nós dois
E a cama de casal eu arrumo depois
E a cama de casal eu arrumo depois
Diz assim, vem!
Não tenho culpa se teu beijo encaixou tão bem
Não tenho culpa se teu beijo encaixou tão bem
Se nossos olhos não tem olhos para mais ninguém
Se meia hora depois que a gente se solta sente saudade
Então, por que não dorme aqui?
Minha camisa pode ser o seu pijama
Se preferir cê pode ficar a semana
Porque por mim você nem ia embora
Muda pra minha vida
E vem se apertar comigo na cama de solteiro
Aqui cabe as suas coisas, nosso amor inteiro
Eu não me importo em ceder espaço pra caber nós dois
Muda pra minha vida
E vem se apertar comigo na cama de solteiro
Aqui cabe as suas coisas, nosso amor inteiro
Eu não me importo em ceder espaço pra caber nós dois
E a cama de casal eu arrumo depois
Yara Tchê, Alessando Costa
Somos nós, Seu Desejo (Seu Desejo)
Diz!
Não tenho culpa se teu beijo encaixou tão bem
Se nossos olhos não tem olhos para mais ninguém
Se meia hora depois que a gente se solta
Escuta assim, ó
Então, por que não dorme aqui?
Minha camisa pode ser o seu pijama
Se preferir cê pode ficar a semana
Porque por mim você nem ia embora
Muda pra minha vida
E vem se apertar comigo na cama de solteiro
Aqui cabe as suas coisas, nosso amor inteiro
Eu não me importo em ceder espaço pra caber nós dois
Muda pra minha vida
E vem se apertar comigo na cama de solteiro
Aqui cabe as suas coisas, nosso amor inteiro
Eu não me importo em ceder espaço pra caber nós dois
E a cama de casal eu arrumo depois
E a cama de casal eu arrumo depois
Diz assim, vem!
Não tenho culpa se teu beijo encaixou tão bem

`).then(e => console.log(`Código finalizado, ${e} mensagens enviadas`)).catch(console.error)

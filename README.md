# HTML Bootcamp #3

I denne opgave skal du arbejde med tilgængelighed (accessibility, a11y).

Tilgængelighed er til for at hjælpe brugere med nedsat evne at navigere og bruge din hjemmeside eller applikation. Specifikationen for tilgængelighed hedder `WAI-ARIA` og er en web-standard, der vedligeholdes og udvikles af W3C. Det er blandt andet denne specifikation, som bestemmer at et `img`-tag skal have en `alt`-attribut.

Kan du forklare hvorfor der skal være en `alt`-attribut på et `img`-tag? Skriv dit svar herunder.

Mit svar:

> Grunden til at der skal være en alt-attribut på et img-tag, kan være flere ting.
> En af tingene er brugervenlighed. Hvis man er skærmlæser og der er en alt-sttribut på et img-tag, kan de derved høre en beskrivelse af hvad der er på billedet eller hvad det skal forestille og derved skabe mere context.
> På knapper ville man skrive en alt tekst der siger "tryk for hjælp", istedet for at beskrive billedet, da det ikke hjælper i denne context.

> Det kan også være til at hjælpe søgemaskiner f.eks Google, til billedsøgning da det giver dem vigtig information om billedet.


## WAI-ARIA

> WAI-ARIA, the Accessible Rich Internet Applications Suite, defines a way to make Web content and Web applications more accessible to people with disabilities. It especially helps with dynamic content and advanced user interface controls developed with Ajax, HTML, JavaScript, and related technologies. Currently certain functionality used in Web sites is not available to some users with disabilities, especially people who rely on screen readers and people who cannot use a mouse. WAI-ARIA addresses these accessibility challenges, for example, by defining new ways for functionality to be provided to assistive technology. With WAI-ARIA, developers can make advanced Web applications accessible and usable to people with disabilities.

https://www.w3.org/WAI/standards-guidelines/aria/

WAI-ARIA implementeres i HTML som attributter på tags, for eksempel:

```html
<button aria-controls="primaryNavigation" aria-describedby="message-menu-button">Menu</button>
<nav id="primaryNavigation" role="navigation" aria-hidden="true">
	<ul>
		<li><a href="#!/forside">Forside</a></li>
		<li><a href="#!/produkter">Produkter</a></li>
		<li><a href="#!/historie">Historie</a></li>
		<li><a href="#!/kontakt">Kontakt</a></li>
	</ul>
</nav>

<div hidden>
	<span id="message-menu-button">Klik her for at vise menuen</span>
</div>
```

I ovenstående eksempel bliver en bruger gjort opmærksom på følgende:
* Der er en knap, som har til opgave at styre et andet objekt (nav-objektet)
* `nav`-objektet har et `landmark`, som fortæller en bruger hvad formålet med objektet er (role="navigation")
* Brugeren bliver gjort opmærksom på, at `nav`-objektet som udgangspunkt er skjult. Det vil sige, at en skærmlæser, for eksempel, vil ignorere dette objekt
* Brugeren for at vide, hvad der vil ske, nå hun klikker på knappen

## Opgave
I filen [index.html](index.html), mangler alle de overordnede semantiske tags.

Du skal rette filen til, så den bliver semantisk korrekt og du skal tilføje tilgængeligheds-attributter, så filen er lettere at bruge for folk med nedsat evne.

### Aflevering
Du skal aflevere på GitHub gennem en pull-request. Husk at pushe ofte.

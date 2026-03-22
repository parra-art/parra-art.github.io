# Sito Parra — Istruzioni

## Struttura cartelle

```
parra.github.io/
├── index.html
├── dipinti.html
├── sculture.html
├── chi-sono.html
├── contatti.html
├── style.css
└── img/
    ├── dipinti/
    │   ├── mediterraneo.jpg
    │   ├── shoah.jpg
    │   └── [altre opere].jpg
    └── sculture/
        ├── rapace.jpg
        ├── tre-piramidi.jpg
        └── [altre sculture].jpg
```

## Come aggiungere un'opera

### Dipinti (dipinti.html)
Copia e incolla questo blocco nella griglia, cambiando i dati:

```html
<div class="art-card fade-in" onclick="openLightbox({
  img: 'img/dipinti/NOME-FILE.jpg',
  titolo: 'Titolo Opera',
  anno: '2024',
  tecnica: 'Olio su tela',
  dimensioni: '60 × 80 cm',
  stato: 'Collezione privata'
})">
  <div class="art-card-img">
    <img src="img/dipinti/NOME-FILE.jpg" alt="Titolo Opera" loading="lazy">
  </div>
  <div class="art-card-info">
    <div class="titolo">Titolo Opera</div>
    <div class="meta">2024 · Olio su tela · 60 × 80 cm</div>
  </div>
</div>
```

### Sculture (sculture.html)
Stesso blocco ma con classe `scultura` sulla card:

```html
<div class="art-card scultura fade-in" onclick="openLightbox({...})">
```

## Ottimizzazione immagini
Prima di caricare le foto su GitHub:
- Ridimensiona a max 1800px sul lato lungo
- Comprimi con tinypng.com o squoosh.app
- Salva in formato JPG, qualità 80-85%

## Personalizzazioni rapide

- **Colore principale (blu)**: cerca `#1a1f6e` in style.css
- **Colore accento (arancio)**: cerca `#e8520a` in style.css
- **Font**: importati da Google Fonts — Cinzel + Cormorant Garamond
- **Email nella pagina contatti**: sostituisci `parra [at] email.it` con la tua email reale

## Lightbox
Clic su qualsiasi opera → si apre il lightbox con immagine grande e scheda tecnica.
Chiudi con: clic fuori dall'immagine, clic su "✕ CHIUDI", o tasto Escape.

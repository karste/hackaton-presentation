# After Effects + Bodymovin + Lottie

Enkel animasjon på alle plattformer

---

### Hva jobbet vi med?
###### (Alexander, Eivind, Karl M)
- Vi har testet rammeverk som forenkler animasjon.
- Eksportering fra After Effects via plugin
- Lottie (Airbnb) + Bodymovin
- Instrukser for animasjon lagres i JSON-filer, og kan distribueres på valgfri måte.

---

### Hvorfor?

- Forenkling av animasjon, spesielt på android og ios
- Animasjonsinstrukser kan deles uavhengig av plattform
- Animasjon er gøy (og viktig):
    + Tiltrekker oppmerksomhet
    + Gir bruker hint
    + Hjelper bruker til å orientere seg
    + Gir feedback på det man gjør
    + Gjør innhold enklere å konsumere
    + Økt forståelse av innhold

---

### Workflow

- Animere i After Effects
    + Bodymovin plugin eksporterer JSON-fil
- Eksponere JSON-fil via rest-api
- Applikasjoner (web og native) kan importere JSON og vise animasjon


---?image=./img/white.png
![Workflow](./img/illustration.png)

---?image=./img/white.png
### ANDROID

```xml
<com.airbnb.lottie.LottieAnimationView
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/animation_view"
    android:layout_width="wrap_content"
    android:layout_height="90dp"
    android:layout_marginTop="20dp"
    android:layout_centerHorizontal="true"
    app:lottie_fileName="paraply.json"
    android:layout_below="@id/pin_input_field_layout"
    app:lottie_loop="true"/>
```

---?image=./img/white.png
### Javascript

```
const params = {
    container: document.getElementById('bodymovin-umbrella'),
    renderer: 'svg',
    loop: 2,
    autoplay: true,
    animationData: json
};
bodymovin.loadAnimation(params);
```


---

# DEMO
- Alle animasjoner på egen rest-server
- Forenklet AB-testing av animasjon

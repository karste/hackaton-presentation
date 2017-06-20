# After Effects + Bodymovin + Lottie

Enkel animasjon på alle plattformer

---

### Hva jobbet vi med?

- Vi testet rammeverk som forenkler animasjon. Instrukser for animasjon lagres i JSON-filer, og kan distribueres på valgfri måte.
- Lottie (Airbnb) + Bodymovin

- Alexander Schipper (designer)
- Eivind Wikheim (utvikler)
- Karl Stenersen (utvikler)

---

### Workflow

- Animere i After Effects
    + Bodymovin eksportere JSON-fil
- Eksponere JSON-fil via rest-api
- Applikasjoner (web og native) kan importere JSON og vise animasjon


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

---?image=./img/white.png
![Workflow](./img/illustration.png)

---

# DEMO

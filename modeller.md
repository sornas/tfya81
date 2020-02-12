## Dimensionsanalys
- Olika enheter för samma storlek (ex fot, meter mäter båda längd) med olika
  användningsområden (sjömil på vatten, AU i rymden osv)
- Dimension är lite mer abstrakt. Behöver skilja på storheter, man kan inte
  använda kilogram för att mäta längd.
- Ex: samband mellan sträcka (s), hastighet (v) och tid (t) med SI-enheterna m,
  m/s, s. Välbekant att s = vt. Vad händer med andra enheter, ex s' i mil, v'
  km/h, t' minuter?
  - Vill omvandla till SI-enheter. 
    - s = 10000 * s'.
    - v = 1000 / (60 * 60) * v'
    - t = 60 * t'.
  - Ganska skitiga konverteringar. Använd alltid SI-enheter i labben.
- Sju grundläggande SI-enheter för sju olika dimensioner. l, m, t vanligast i
  grundläggande labbar. Historiska definitioner, omdefinierade 2019.
- Resterande enheter härldes ur grundenheterna, ex hastighet, kraft, energi osv.
- Samma dimension i HL och VL i en formel (om det är en riktig formel).
- Inte nödvändigt att alla dimensionskorrekta formler är riktiga formler (alltså
  inte ett ekvivalenspåstående).
- Finns några regler
  - För summasamband: varje term måste ha rätt dimension. Ex. s = v\_0 * t + at^2 / 2.
  - Elementära funktioner har, eftersom de approximeras av oändliga polynom,
    dimensionen 1 inuti. Alltså om ln(x), sin(x), e^x ... => dim(x) == 1.
  - Dimensionsmässigt: dim(sqrt(x^2 + y^2 + z^2)) == dim(sqrt(x^2)) == dim(x) == L.
  - etc
- Kan kontrollera ett samband (inte lika elegant) med enheter istället för
  dimension, ex kraftekvationen F = ma.
- Enklast om vi har ett produktsamband som hypotes.
- EXEMPEL: Dimensionsanalys av en liten massa som pendlar.
  - Vad kan tänkas påverka periodtiden?
    - massa
    - tyngdacceleration
    - snörlängd
    - svängningstid
    - utgångsvinkeln (dimensionslös!)
  - Ansats: T(l, m, g) = C * l^x * m^y * g^z
    - Dimensionsekvation: T = L^x * M^y * (LT^-2)^z
      <=> T^1 * M^0 * L^0 = T^-2z * M^y * L^x+z
      <=> y = 0, z = -1/2, x = 1/2
      <=> T(l, m, g) = C * sqrt(l/g)
- EXEMPEL: mer komplext, balkens nedböjning.
  - Komplext ekvationssystem med tre ekvationer (dimensionssamband) men sex
    okända (exponenter, ingående storheter).
  - Ingen entydig lösning, däremot får vi lösning om vi hittar tre exponenter på
    annan väg genom ex. linjärisering.

## Linjärisering
- Vill skriva om uttryck till y = kx + m.
- EXEMPEL: Antag potenssambandet T = C * L^k
  - <=> ln(T) = ln(C * L^k) = k * ln(L) + ln(C)
- Tillbaka till balkens nedböjning: Variera endast b: d = c\_b * b^v
  - <=> ln(d) = v * ln(b) + ln(c\_b)
  - Anpassa en rät linje, se att den räta linjen har y = -0.97x - 5.16. Rimligt
    att avrunda till ett snyggt och fint rationellt tal, i det här fallet v =
    -1.
- Sedan variera andra variabler tills dimensionsanalysen fixar biffen.
- Fysiker tenderar att leta linjära samband eftersom de är trevliga. Undersök
  små värden eftersom ex. sqrt är väldigt lik linjära samband för icke-små x.
- EXEMPEL: Radioaktivt sönderfall. N = N\_0 * e^(-lambda * t)
  - <=> ln(N) = -lambda * t + ln(N\_0)

## Linjärisering av summauttryck
- Om x -/-> 0/inf när x-->0 så kan det inte vara ett produktsamband.
- För större x kommer (förhoppningsvis) den ingående resterande summan vara
  försumbar.
- Behöver kunna jämföra y = D * sqrt(x) + C och y = sqrt(Dx + C)
  - Testa rita graf med y=y och x=sqrt(x) och rita/jämför med y=y^2, x = Dx + C

## Konstanter
- Än en gång ett antal tester med olika värden, sedan antingen medelvärde eller
  linjärisering och lutning / intercept (om ln).

## Mätningar
- Hur tar man fram kompletta modeller från enklare mätningar och resultat?
- Saker att tänka på:
  - Minimera fel
  - Maxmiera noggranhet
  - Fundera över möjligheter att öka precisionen:
    - Längre snören för mer exakt mätdata.
    - Mät 10 pendelingar och dividera med 10.
    - Mät flera gånger och ta medelvärde.
- Alla mätningar har osäkerhet!
- Använd inte orimligt många värdesiffror, 6.2 = 6.20 ± 0.5.
- Oftare mer relevant med relativ mätosäkerhet (∆M / M). 1m ± 1cm => 1%,
  100m ±1cm => 0.01%.
- Felfortplantningsformeln.

## Rapport
- Kolla rapportmallen
- Kolla rättningsprotokollet (innan inlämning!)

# Prelucrare-Grafica-proiect
 
Proiectul are ca și scop realizarea unei prezentări fotorealiste a unor scene de obiecte 3D utilizând librăriile OpenGl, GLFW, GLM, etc. . 

![image](https://github.com/maiercristinaa/Prelucrare-Grafica-proiect/assets/164372227/9ee878b4-a975-4bb6-8fef-fc6d8629add2)

![image](https://github.com/maiercristinaa/Prelucrare-Grafica-proiect/assets/164372227/d7b2c9a4-a095-452a-bbe8-9f188b08a6b0)

![image](https://github.com/maiercristinaa/Prelucrare-Grafica-proiect/assets/164372227/a7cc0526-70ba-4767-a3c5-a4a86961a424)

In implementarea proiectului am folosit diferiti algoritmi pentru implementarea diferitelor functionalitati precum animatii, ceata, animatii de miscare , miscarea si rotatia camerei. 
Pentru efectul de ceata am folosit metoda explonentiala patratica de creare a cetei mai exact : 𝑓𝑜𝑔𝐹𝑎𝑐𝑡𝑜𝑟 = 𝑒 ^−(𝑓𝑟𝑎𝑔𝑚𝑒𝑛𝑡𝐷𝑖𝑠𝑡𝑎𝑛𝑐𝑒 ∗ 𝑓𝑜𝑔𝐷𝑒𝑛𝑠𝑖𝑡𝑦) ^2.
Prin creare efectului de ceata am reusit sa creez o atmosfera speciala astfel incat cu cat ma indepartez mai tare de un obiect acesta dispare in “ceata”.
Animarea obiectelor am realizat-o cu ajutorul miscarilor de translatie si rotatie.
Efectul de light On / Off este realizat cu o variabilă uniform care e true sau false atunci când se apasă pe tasta corespunzătoare.

Algoritmi:

•	Luminile punctiforme sunt surse de lumină cu o localizare specifică care proiectează iluminare într-un mod radial și uniform în toate direcțiile. Spre deosebire de lumina direcțională, razele emise de sursele luminoase punctiforme se estompează în funcție de distanță, creând o distribuție variabilă de lumină. Această abordare conferă obiectelor apropiate de sursă o iluminare mai intensă decât obiectelor aflate mai îndepărtate. Folosirea surselor de lumină punctiforme implică o variație a direcției luminii între fragmente, iar aceasta trebuie calculată distinct pentru fiecare fragment. Introducerea atenuării pătratice în funcție de distanță sporește semnificativ realismul. Pentru implementarea atenuării, coeficienții corespunzători pot fi definiți în shader sau transmiși prin variabile uniforme din aplicație.

•	Tehnica umbrelor - Shadow mapping este o metodă care se bazează pe texturi de adâncime pentru a determina dacă un punct din scenă se află în umbră sau nu. Această tehnică necesită observarea scenei din perspectiva sursei de lumină în loc de perspectiva camerei. Zonele care nu sunt direct vizibile din punctul de vedere al luminii vor fi considerate în umbră. Procesul implică două etape majore: rasterizarea scenei din punctul de vedere al sursei de lumină (valorile de adâncime fiind stocate într-o hartă de adâncime) și rasterizarea scenei din perspectiva observatorului, unde adâncimea fiecărui fragment vizibil este comparată cu valorile de adâncime din harta umbrelor.

Scena captivantă a fost creată în întregime în Blender, un software de modelare 3D extrem de versatil și puternic. Fiecare detaliu, de la mărețul castel și până la pitorescul lac, a fost sculptat și modelat cu atenție folosind instrumentele precise.

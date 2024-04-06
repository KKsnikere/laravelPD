# Laravel PD

## 1. Kas ir API?
Lietojumprogrammu saskarne (application programming interface) ir noteikumu vai protokolu kopums, kas ļauj programmatūras lietojumprogrammām sazināties savā starpā, lai apmainītos ar datiem, līdzekļiem un funkcionalitāti.

## 2. Kā deklarēt mainīgo PHP valodā?
PHP mainīgais sākas ar $ zīmi, kam seko mainīgā nosaukums: 

*$x = 3;*
*$y = "Kartupelis"*

## 3. Kādu arhitektūru izmanto Laravel, paskaidro kā tā strādā?
Model-View-Controller (MVC) arhitektūra. Šī arhitektūra atdala biznesa loģiku no prezentācijas loģikas, padarot kodu tīrāku, vieglāk pārvaldāmu un vieglāk uzturējamu.
* Modelis: attēlo datu struktūru, parasti kartējot datu bāzes tabulās. Programmā Laravel modeļi tiek izmantoti, lai mijiedarbotos ar datu bāzi, izpildītu vaicājumus un definētu attiecības starp dažādām tabulām.
* Skats: šis ir lietojumprogrammas prezentācijas slānis. Programmā Laravel skati parasti tiek veidoti, izmantojot Blade, Laravel jaudīgo veidņu dzinēju, kas ļauj tīrā un sakārtotā veidā iekļaut PHP kodu.
* Kontrolieris: Kontrolieri darbojas kā starpnieki starp modeļiem un skatiem. Viņi kontrolē datu plūsmu uz modeļiem un izlemj, kuru skatu parādīt lietotājam.
  
## 4. Kas ir ORM, kāpēc to izmanto tīra SQL vietā?
ORM (Object-Relational Mapping) piedāvā elegantu un vienkāršu abstrakciju mijiedarbībai ar datu bāzi. Izmantojot Eloquent, ir viegli veikt CRUD (Create, Read, Update, Delete) darbības un noteikt attiecības starp dažādām datu entītijām. SQL nodrošina precīzu datu bāzes darbību kontroli un ir labi piemērota lietojumprogrammām un mantotajām sistēmām. No otras puses, ORM vienkāršo datu bāzes darbības, saskaņo ar objektu orientēto paradigmu un uzlabo produktivitāti.

## 5. Uzraksti Eloquent ORM pieprasījumu modelim User, kur nepieciešams iegūt visus lietotājus, kuriem reitings ir lielāks par 4.
### $users = User::where('rating', '>', 4)->get();

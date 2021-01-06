## MoWaS_NINA_Analyse_V2

Motiviert durch den [bundesweiten Warntag 2020](https://warnung-der-bevoelkerung.de/) kam initial die Idee auf, zu analysieren, welche Meldungen durch [MoWaS](https://www.bbk.bund.de/DE/AufgabenundAusstattung/Krisenmanagement/WarnungderBevoelkerung/MoWaS/ModularesWarnsystem_node.html) (Modulares Warnsystem) an die Warn-App [NINA](https://www.bbk.bund.de/DE/NINA/Warn-App_NINA_node.html) gesendet wurden. V1 der Analyse wurde anhand von Daten der Jahre 2014-2017 durchgeführt und ist [hier](https://github.com/orSpec/MoWaS_NINA_Analyse) abrufbar.

Aufgrund der veralteten Daten in der ersten Analyse wurden neue Daten beim BBK (Bundesamt für Bevölkerungsschutz und Katastrophenhilfe) angefragt. Das BBK stellte hierzu Daten für den Zeitraum 2015-2020 zur Verfügung. Die Rohdaten sind frei zugänglich auf [FragDenStaat](https://fragdenstaat.de/anfrage/warnmeldungen-uber-die-warn-app-nina/).

Das Jupyter-Notebook, welches die Analyse enthält, kann [hier](https://nbviewer.jupyter.org/github/orSpec/MoWaS_NINA_Analyse_V2/blob/master/analysis/Analyse_Meldungen.ipynb) gerendert betrachtet werden.

### Code
Die Analyse wurde in einem [Jupyter Notebook](https://jupyter.org/) mithilfe der folgenden Bibliotheken durchgeführt:

 - pandas
 - [matplotlib.pyplot](https://matplotlib.org/api/pyplot_api.html) und [seaborn](https://seaborn.pydata.org/) zur Visualisierung
 - [geopy](https://geopy.readthedocs.io/en/stable/#) zur Geokodierung
 - [folium](https://python-visualization.github.io/folium/) zum Erstellen von Karten
 - [wordcloud](http://amueller.github.io/word_cloud/) zum Erstellen einer Wortwolke

### Erkenntnisse
Unter anderem lässt sich aus den Daten erkennen, dass NRW in allen betrachteten Jahren die meisten Warnmeldungen auslöste:
<img src="https://user-images.githubusercontent.com/59450716/102813222-ba1e4c00-43c8-11eb-9184-0d73f62c078f.png" width="1000">

Setzt man allerdings die Anzahl der Warnmeldungen in Bezug zur Einwohnerzahl, so ändert sich das Bild:
<img src="https://user-images.githubusercontent.com/59450716/102813440-17b29880-43c9-11eb-9b70-2bb82b6f6ae5.png" width="1000">
Der Anteil von NRW ist zwar immer noch groß, vor allem in 2017, er dominiert aber nicht alle anderen Bundesländer.

Unter der Annahme, dass die Anzahl der Meldungen pro Einwohner in jedem Land gleichverteilt ist, können Bundesländer identifiziert werden, welche über- bzw. unterproportional oft Alarm schlagen:
<img src="https://user-images.githubusercontent.com/59450716/102813663-7c6df300-43c9-11eb-90fc-9665447f22f3.png" width="1400">
Überproportional häufig vertreten sind hierbei in drei Jahren Bayern, Bremen, Nordrhein-Westfalen, Schleswig-Holstein, Sachsen-Anhalt und Thüringen. Zumindest für NRW könnte dies partiell mit der hohen Industriedichte erklärt werden.

In den Daten ist für die letzten Jahre auch die Kategorie der Warnmeldung enthalten. Häufig Grund der Warnung ist demnach Feuer, Versorgung und Infrastruktur sowie die öffentliche Sicherheit:
<img src="https://user-images.githubusercontent.com/59450716/102814088-4c731f80-43ca-11eb-8d7e-9c042f1474b8.png" width="1400">



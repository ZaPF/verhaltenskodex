# Verhaltenskodex der ZaPF

Dieses Repository enthält die Quelldateien für den Verhaltenskodex der ZaPF.

## Homepage

* <https://zapf.wiki/Verhaltenskodex>

## Kontakt

* [Ständiger Ausschuss der Physik-Fachschaften – kurz StAPF](http://zapfev.de/zapf/stapf)
  * E-Mail: **stapf@zapf.in**

## Wegweise

Die `main` branch enthält die offiziele Variante des Verhaltenskodex in
Markdown. Aus
dieser können mit pandoc die Versionen in [HTML](./versions/verhaltenskodex.html) und
[LaTeX](./versions/verhaltenskodex.tex) und daraus die
[PDF-Version](./versions/verhaltenskodex.pdf) sowie die Version in
[Mediawiki-Markup](./versions/verhaltenskodex.wiki) generiert werden.

Die Versionen werden immer nach einer ZaPF, auf deren Abschlussplenum die
Verhaltenskodex geändert wurde, nachdem diese als [Pull
Requests](https://github.com/ZaPF/verhaltenskodex/pulls) gemergt wurden und [der
Änderungsvermerkt](./verhaltenskodex.md#%20%C3%84nderungshistorie) hinzugefügt
wurde, neu generiert.

Um die Versionen neu zu generieren führt man den Befehl
```bash
make -C util
```
aus. Was dabei passiert, kann man im [Makefile](./util/Makefile) sehen.

Ein Beispiel für einen Commit, in dem der Änderungsvemerkt hinzugefügt wird und
die neu generierten Versionen hinzugefügt werden, ist
[dieser](https://github.com/ZaPF/verhaltenskodex/commit/a1f3239c29c410c20ed3063615a83331e42b1e39).

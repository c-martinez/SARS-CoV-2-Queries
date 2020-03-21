# virusGenes.rq
**Code examples:** [curl](#curl)
### SPARQL
```sparql
SELECT ?gene ?geneLabel ?ncbi WHERE {
  ?gene wdt:P703 wd:Q82069695 ; wdt:P31 wd:Q7187 .
  OPTIONAL { ?gene wdt:P351 ?ncbi }
  SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
}
```
[Execute](https://query.wikidata.org/embed.html#SELECT%20%3Fgene%20%3FgeneLabel%20%3Fncbi%20WHERE%20%7B%0A%20%20%3Fgene%20wdt%3AP703%20wd%3AQ82069695%20%3B%20wdt%3AP31%20wd%3AQ7187%20.%0A%20%20OPTIONAL%20%7B%20%3Fgene%20wdt%3AP351%20%3Fncbi%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%2Cen%22.%20%7D%0A%7D%0A) or [Edit](https://query.wikidata.org/#SELECT%20%3Fgene%20%3FgeneLabel%20%3Fncbi%20WHERE%20%7B%0A%20%20%3Fgene%20wdt%3AP703%20wd%3AQ82069695%20%3B%20wdt%3AP31%20wd%3AQ7187%20.%0A%20%20OPTIONAL%20%7B%20%3Fgene%20wdt%3AP351%20%3Fncbi%20%7D%0A%20%20SERVICE%20wikibase%3Alabel%20%7B%20bd%3AserviceParam%20wikibase%3Alanguage%20%22%5BAUTO_LANGUAGE%5D%2Cen%22.%20%7D%0A%7D%0A)


### Output
<table>
  <tr>
    <td><b>gene</b></td>
    <td><b>ncbi</b></td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88000922">S surface glycoprotein of SARS-CoV-2</a> (<a href="http://www.wikidata.org/entity/Q88000922">edit</a>)</td>
    <td>43740568</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88088053">orf1a polyprotein;orf1ab polyprotein</a> (<a href="http://www.wikidata.org/entity/Q88088053">edit</a>)</td>
    <td>43740578</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88088595">ORF3a protein</a> (<a href="http://www.wikidata.org/entity/Q88088595">edit</a>)</td>
    <td>43740569</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88088888">envelope protein</a> (<a href="http://www.wikidata.org/entity/Q88088888">edit</a>)</td>
    <td>43740570</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88089048">membrane glycoprotein</a> (<a href="http://www.wikidata.org/entity/Q88089048">edit</a>)</td>
    <td>43740571</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88089203">ORF6 protein</a> (<a href="http://www.wikidata.org/entity/Q88089203">edit</a>)</td>
    <td>43740572</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88089283">ORF7a protein</a> (<a href="http://www.wikidata.org/entity/Q88089283">edit</a>)</td>
    <td>43740573</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88089438">ORF7b</a> (<a href="http://www.wikidata.org/entity/Q88089438">edit</a>)</td>
    <td>43740574</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88089552">ORF8 protein</a> (<a href="http://www.wikidata.org/entity/Q88089552">edit</a>)</td>
    <td>43740577</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88089689">nucleocapsid phosphoprotein</a> (<a href="http://www.wikidata.org/entity/Q88089689">edit</a>)</td>
    <td>43740575</td>
  </tr>
  <tr>
    <td><a href="https://tools.wmflabs.org/scholia/Q88105063">GeneRIF placeholder gene for SARS-CoV-2</a> (<a href="http://www.wikidata.org/entity/Q88105063">edit</a>)</td>
    <td>43562271</td>
  </tr>
</table>
## Code examples
### curl
```shell
curl -o virusGenes.rq https://raw.githubusercontent.com/egonw/SARS-CoV-2-Queries/master/sparql/virusGenes.rq
curl -H "Accept: text/tab-separated-values" -G https://query.wikidata.org/bigdata/namespace/wdq/sparql --data-urlencode query@virusGenes.rq
```
This SPARQL query is available under CCZero.
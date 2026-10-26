# README


## XGBOOST RESULTS

``` python
import pandas as pd
from IPython.display import Markdown

fc = pd.read_csv("forecast_ppa_2026.csv")

top = (fc.sort_values("pred_ppa_2026", ascending=False)  
         .head(25)
         .round(3)
         .reset_index(drop=True))
top.index += 1  

Markdown(top.to_markdown())
```

<table>
<colgroup>
<col style="width: 4%" />
<col style="width: 20%" />
<col style="width: 16%" />
<col style="width: 12%" />
<col style="width: 15%" />
<col style="width: 12%" />
<col style="width: 17%" />
</colgroup>
<thead>
<tr>
<th style="text-align: right;"></th>
<th style="text-align: left;">name</th>
<th style="text-align: left;">team</th>
<th style="text-align: left;">position</th>
<th style="text-align: right;">usg_overall</th>
<th style="text-align: right;">ppa_2025</th>
<th style="text-align: right;">pred_ppa_2026</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: right;">1</td>
<td style="text-align: left;">Adam Criter</td>
<td style="text-align: left;">San Diego</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.25</td>
<td style="text-align: right;">0.072</td>
<td style="text-align: right;">2.358</td>
</tr>
<tr>
<td style="text-align: right;">2</td>
<td style="text-align: left;">Michael Wortham</td>
<td style="text-align: left;">Montana</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.157</td>
<td style="text-align: right;">0.583</td>
<td style="text-align: right;">2.353</td>
</tr>
<tr>
<td style="text-align: right;">3</td>
<td style="text-align: left;">Ryan Jezioro</td>
<td style="text-align: left;">Idaho</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.08</td>
<td style="text-align: right;">0.509</td>
<td style="text-align: right;">1.005</td>
</tr>
<tr>
<td style="text-align: right;">4</td>
<td style="text-align: left;">BJ Fleming</td>
<td style="text-align: left;">North Dakota</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.096</td>
<td style="text-align: right;">0.699</td>
<td style="text-align: right;">1.004</td>
</tr>
<tr>
<td style="text-align: right;">5</td>
<td style="text-align: left;">Fidel Tau Pitts</td>
<td style="text-align: left;">Cal Poly</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.061</td>
<td style="text-align: right;">1.307</td>
<td style="text-align: right;">0.985</td>
</tr>
<tr>
<td style="text-align: right;">6</td>
<td style="text-align: left;">John Anthony</td>
<td style="text-align: left;">Lindenwood</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.149</td>
<td style="text-align: right;">0.529</td>
<td style="text-align: right;">0.973</td>
</tr>
<tr>
<td style="text-align: right;">7</td>
<td style="text-align: left;">Malik Benson</td>
<td style="text-align: left;">Oregon</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.061</td>
<td style="text-align: right;">0.841</td>
<td style="text-align: right;">0.971</td>
</tr>
<tr>
<td style="text-align: right;">8</td>
<td style="text-align: left;">Kobe Prentice</td>
<td style="text-align: left;">Baylor</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.046</td>
<td style="text-align: right;">0.804</td>
<td style="text-align: right;">0.963</td>
</tr>
<tr>
<td style="text-align: right;">9</td>
<td style="text-align: left;">J.J. Evans</td>
<td style="text-align: left;">Norfolk State</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.078</td>
<td style="text-align: right;">0.656</td>
<td style="text-align: right;">0.961</td>
</tr>
<tr>
<td style="text-align: right;">10</td>
<td style="text-align: left;">Justin Olson</td>
<td style="text-align: left;">Charlotte</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.054</td>
<td style="text-align: right;">0.152</td>
<td style="text-align: right;">0.961</td>
</tr>
<tr>
<td style="text-align: right;">11</td>
<td style="text-align: left;">Charlie Becker</td>
<td style="text-align: left;">Indiana</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.053</td>
<td style="text-align: right;">1.254</td>
<td style="text-align: right;">0.96</td>
</tr>
<tr>
<td style="text-align: right;">12</td>
<td style="text-align: left;">Cincere Gill</td>
<td style="text-align: left;">Presbyterian</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.072</td>
<td style="text-align: right;">1.468</td>
<td style="text-align: right;">0.959</td>
</tr>
<tr>
<td style="text-align: right;">13</td>
<td style="text-align: left;">Davion Dozier</td>
<td style="text-align: left;">App State</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.079</td>
<td style="text-align: right;">0.645</td>
<td style="text-align: right;">0.951</td>
</tr>
<tr>
<td style="text-align: right;">14</td>
<td style="text-align: left;">Dkhai Joseph</td>
<td style="text-align: left;">SE Louisiana</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.036</td>
<td style="text-align: right;">0.158</td>
<td style="text-align: right;">0.949</td>
</tr>
<tr>
<td style="text-align: right;">15</td>
<td style="text-align: left;">Kevin Concepcion</td>
<td style="text-align: left;">Texas A&amp;M</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.119</td>
<td style="text-align: right;">0.593</td>
<td style="text-align: right;">0.945</td>
</tr>
<tr>
<td style="text-align: right;">16</td>
<td style="text-align: left;">Noah Thomas</td>
<td style="text-align: left;">Georgia</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.036</td>
<td style="text-align: right;">0.681</td>
<td style="text-align: right;">0.945</td>
</tr>
<tr>
<td style="text-align: right;">17</td>
<td style="text-align: left;">Isaiah Horton</td>
<td style="text-align: left;">Alabama</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.061</td>
<td style="text-align: right;">0.971</td>
<td style="text-align: right;">0.943</td>
</tr>
<tr>
<td style="text-align: right;">18</td>
<td style="text-align: left;">Tony Johnson</td>
<td style="text-align: left;">Miami</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.031</td>
<td style="text-align: right;">0.629</td>
<td style="text-align: right;">0.94</td>
</tr>
<tr>
<td style="text-align: right;">19</td>
<td style="text-align: left;">Carnell Tate</td>
<td style="text-align: left;">Ohio State</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.099</td>
<td style="text-align: right;">1.113</td>
<td style="text-align: right;">0.94</td>
</tr>
<tr>
<td style="text-align: right;">20</td>
<td style="text-align: left;">Ryan Tattersall</td>
<td style="text-align: left;">Harvard</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.062</td>
<td style="text-align: right;">0.861</td>
<td style="text-align: right;">0.939</td>
</tr>
<tr>
<td style="text-align: right;">21</td>
<td style="text-align: left;">Ben Ford</td>
<td style="text-align: left;">Boise State</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.063</td>
<td style="text-align: right;">1.169</td>
<td style="text-align: right;">0.939</td>
</tr>
<tr>
<td style="text-align: right;">22</td>
<td style="text-align: left;">Rashad Rochelle</td>
<td style="text-align: left;">Indiana State</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.101</td>
<td style="text-align: right;">0.918</td>
<td style="text-align: right;">0.938</td>
</tr>
<tr>
<td style="text-align: right;">23</td>
<td style="text-align: left;">Shazz Preston</td>
<td style="text-align: left;">Tulane</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.062</td>
<td style="text-align: right;">0.933</td>
<td style="text-align: right;">0.937</td>
</tr>
<tr>
<td style="text-align: right;">24</td>
<td style="text-align: left;">Roriyon Richardson</td>
<td style="text-align: left;">Texas Southern</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.071</td>
<td style="text-align: right;">0.783</td>
<td style="text-align: right;">0.937</td>
</tr>
<tr>
<td style="text-align: right;">25</td>
<td style="text-align: left;">Tanook Hines</td>
<td style="text-align: left;">USC</td>
<td style="text-align: left;">WR</td>
<td style="text-align: right;">0.056</td>
<td style="text-align: right;">1.011</td>
<td style="text-align: right;">0.936</td>
</tr>
</tbody>
</table>

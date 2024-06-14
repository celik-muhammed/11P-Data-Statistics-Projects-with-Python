### [Go to Home Page](https://github.com/celik-muhammed)

<div align="center">
  
| [![](https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white)][Linkedin] | [<img src="https://www.kaggle.com/static/images/site-logo.svg" alt="kaggle" height="28.5"/>][kaggle] | [<img src="https://www.tableau.com/sites/default/files/2021-05/tableau_rgb_500x104.png" alt="tableau" height="50"/>][tableau] | [<picture><source media="(prefers-color-scheme: dark)" srcset="https://theme.zdassets.com/theme_assets/224203/4a55138e21ad44a9c72c8295181c79fe938a2ae6.svg" alt="kaggle" height="26"><img alt="Dark" src="https://cdn-static-1.medium.com/sites/medium.com/about/images/Medium-Logo-Black-RGB-1.svg" alt="kaggle" height="26"></picture>][medium] | [<img src="https://user-images.githubusercontent.com/94930605/160260064-ff3aa908-cbfd-4350-ab28-a26a0b7a1819.png" alt="github_pages" height="28.5"/>][github_pages] |
|:-:|:-:|:-:|:-:|:-:|
<!-- CHANGE-05 .../myname/ myname yerine profil user name yaz -->
[Linkedin]: https://www.linkedin.com/in/çelik-muhammed/ "LinkedIn"
[kaggle]: https://www.kaggle.com/clkmuhammed "Kaggle Page"
[tableau]: https://public.tableau.com/app/profile/celikmuhammed "Tableau Page"
[medium]: https://celik-muhammed.medium.com/ "Medium Page"
[github_pages]: https://celik-muhammed.github.io/ "GitHub Pages"
</div>

<table align="center">
    <caption><div align='center'>Data Statistics Projects with Python</div></caption>
<thead align='left'><tr><th>Statistics</th></tr></thead>
<tbody>
<tr>
  <td>
<!--     <a href="#">01. Statistics</a> -->
  </td>
</tr>
</tbody>
  
<tfoot>
  <tr><td>draft</td></tr>
</tfoot>
</table>


<div align='center'><img src='https://images.squarespace-cdn.com/content/v1/64c4f5cffc1a5952f996c322/9bf085ec-4546-476c-b132-02705ed9adff/p-value.png'></div>



<h1>Understanding p-Value and Its Role in Statistical Tests</h1>

<h2>What is a p-Value?</h2>

<ul>
  <li><strong>Definition:</strong> The p-value is a probability measure that helps determine the significance of the results obtained from a statistical test. It quantifies the evidence against the null hypothesis ( H_0 ).</li>
  <li><strong>Range:</strong> The p-value ranges between 0 and 1.</li>
  <li><strong>Interpretation:</strong>
    <ul>
      <li><strong>Low p-value (typically &lt; α):</strong> Strong evidence against the null hypothesis, leading to rejection of ( H_0 ) in favor of ( H_1 ).</li>
      <li><strong>High p-value (typically &ge; α):</strong> Weak evidence against the null hypothesis, leading to failure to reject ( H_0 ).</li>
    </ul>
  </li>
  <li><strong>Key Points:</strong>
    <ul>
      <li><strong>Significance Level:</strong> Choose a significance level (𝛼) before conducting the test (commonly 0.05).</li>
      <li><strong>Decision Rule:</strong> If p-value &lt; α, reject ( H_0 ), if p-value &ge; α, fail to reject ( H_0 ).</li>
    </ul>
</ul>

<h2>How to Use p-Value in Statistical Tests</h2>

<!--
Greater than: &gt; or >
Less than: &lt; or <
Greater than or equal to: &ge; or >=
Less than or equal to: &le; or <=
-->
<ol>
  <li><strong>Formulate Hypotheses:</strong>
    <ul>
      <li><strong>Null Hypothesis ( H_0 ):</strong> No effect or no difference.</li>
      <li><strong>Alternative Hypothesis ( H_1 ):</strong> Some effect or difference.</li>
    </ul>
  </li>
  <li><strong>Choose Significance Level ( alpha ):</strong> Commonly set at 0.05, 0.01, or 0.10.</li>
  <li><strong>Conduct the Statistical Test:</strong> Calculate the test statistic and the corresponding p-value.</li>
  <li><strong>Compare p-Value with α:</strong>
    <ul>
      <li>If  p-value &lt; alpha : Reject  ( H_0 ). The results are statistically significant.</li>
      <li>If  p-value &ge; alpha : Fail to reject  ( H_0 ). The results are not statistically significant.</li>
    </ul>
  </li>
</ol>

<h2>Basic Concepts of  ( H_0 )  and  ( H_1 ) </h2>

<h3>Null Hypothesis ( H_0 )</h3>

<ul>
  <li><strong>Definition:</strong> The null hypothesis states that there is <strong>no effect or no difference</strong>. It serves as the <strong>default or starting assumption</strong>.</li>
  <li><strong>Example:</strong>  ( H_0 ) : The mean score of two groups is equal.</li>
</ul>

<h3>Alternative Hypothesis ( H_1 )</h3>

<ul>
  <li><strong>Definition:</strong> The alternative hypothesis states that <strong>there is an effect or a difference</strong>. It is what the researcher aims to prove.</li>
  <li><strong>Example:</strong>  ( H_1 ) : The mean score of two groups is different.</li>
</ul>

<h2>Using Statistical Tests to Evaluate Hypotheses</h2>

<ol>
  <li><strong>Choose the Appropriate Test:</strong> Depending on the data type and research question (e.g., t-test for means, chi-square test for independence).</li>
  <li><strong>Set Up the Hypotheses:</strong> Null and alternative hypotheses based on the research question.</li>
  <li><strong>Calculate the Test Statistic and p-Value:</strong> Use statistical software or libraries like SciPy in Python.</li>
  <li><strong>Make a Decision:</strong>
    <ul>
      <li>Compare the p-value with the chosen significance level alpha .</li>
    </ul>
  </li>
</ol>

<h2>Practical Application Example</h2>

<pre><code>## Common Tests:
## t-tests: Compare means of two groups.
## ANOVA: Compare means of more than two groups.
## Chi-square test: Assess independence between categorical variables.
## Correlation tests: Assess relationships between variables 
## (e.g., Pearson correlation, Spearman correlation, Partial correlation).
from scipy.stats import ttest_ind

## Sample data
group1 = [23, 21, 18, 30, 28]
group2 = [25, 27, 22, 31, 33]

## Conduct t-test
t_stat, p_value = ttest_ind(group1, group2)

## Print results
print(f"t-statistic: {t_stat}, p-value: {p_value}")

## Interpret p-value
alpha = 0.05
if p_value <= alpha:
    print("Reject the null hypothesis. There is a significant difference between the groups.")
else:
    print("Fail to reject the null hypothesis. There is no significant difference between the groups.")  
</code></pre>

<h2>Summary</h2>

<ul>
  <li>The <strong>p-value</strong> helps determine the statistical significance of test results.</li>
  <li><strong>Null Hypothesis ( H_0 )</strong>: Assumes no effect or no difference.</li>
  <li><strong>Alternative Hypothesis ( H_1 )</strong>: Assumes some effect or difference.</li>
  <li><strong>Significance Level ( alpha )</strong>: Threshold for deciding whether to reject  H_0 .</li>
  <li>Use statistical tests to calculate p-values and make informed decisions based on the data.</li>
</ul>

<p>By understanding these concepts and following the outlined steps, you can effectively use p-values and statistical tests to evaluate hypotheses and make data-driven decisions.</p>




> There are various distribution but the major distribution used in data science are :
>> [Statistical Distributions](https://mathworld.wolfram.com/topics/StatisticalDistributions.html)<br>
>> [Family of Distribution](http://www.machineintellegence.com/distributions/)

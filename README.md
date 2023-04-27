
<h1> Portfolio Theory Basics: The Efficient Frontier, the CAPM, and the Sharpe Ratio</h1>
<p> In this project I outline the beginning foundation of modern portfolio theory and its underlying basics. I calculate and graph key portfolio performance indicators - the Efficient Frontier, the CAPM, and the Sharpe Ratio - using Python. Hopefully this highlights how powerful, efficient, and informative using programming is for financial analysis.</p>
<br>
<h2>Markowitz's Efficient Frontier</h2>
<p>Harry Markowitz was an American economist that created the <i>Efficient Frontier</i> model in 1952. This model finds optimal asset portfolios that give the highest returns with minimal risk. To achieve this optimal portfolio, different weights for assets in the portfolio are used to produce desired returns. This concept is central to the risk-return trade-off at the cornerstone of modern portfolio management philosophies.

<p>To find the Efficient Frontier, also known as Markowitz's Bullet, we plot the Expected Return on the y-axis and the Portfolio Risk (as Standard Deviation) on the x-axis.
    
<p>To calculate the Expected Return we use the formula below:
    <p>$R = (w_{1}*r_{1}) + (w_{2}*r_{2}) + (w_{3}*r_{3}) + ...$
    <ul> 
    <li> Expected Return ($R$)
    <li> Portfolio Weight of Asset ($w_{x}$) 
    <li> Rate of Return of Asset ($r_{x}$)
    </ul>
<p>By using this formula with various assets' weights we can calculate different Expected Returns for a portfolio.
<p>To calculate the Portfolio Risk we use the formula below:
    <p>$\sigma P = \sqrt{(w_{1}^{2}*\sigma_{1}^{2})+(w_{2}^{2}*\sigma_{2}^{2})+((2*Corr)*\sigma_{1}*\sigma_{2}})$
    <ul> 
    <li> Portfolio Risk ($\sigma P$)
    <li> Portfolio Weight of Asset ($w_{x}$) 
    <li> Standard Deviation of Asset ($\sigma_{x}$)
    <li> Correlation Coefficient ($Corr$)
    </ul>
<p> Lucky for us, all these calculations can be handled using Python. I demonstrate this in the attached Jupyter notebook.
<br>
<h2>The Capital Asset Pricing Model</h2>
<p> The <i>Capital Assest Pricing Model</i> (CAPM) formula:
       <p> $r_{i} = r_{f} + \beta_{im}(r_{m}-r_{f})$

<p> The CAPM is a measure of the the risk and return of a security investment. There are three essential components to the CAPM:
    <ul>
    <li> Risk-Free Return ($r_{f}$)
    <li> Market Risk Premium ($r_{m}-r_{f}$) 
    <li> Beta of the investment ($\beta_{im}$)
    </ul>
    <p>The <i>Risk-Free Return</i> ($r_{f}$) is the value of an investment that carries zero risk. In reality there is no investment that carries a true risk rate equal to zero. A close investment that actually nears zero is the US 10-year government bond. This is because the US government is extremely unlikely not to pay back its bond holders - hence the near risk-free status and why it is often used in CAPM calculations for US markets.
<p>The <i> Market Risk Premium</i> $(r_{m}-r_{f})$ is the return that is expected from the portfolio beyond the risk-free assets. This premium rate is a strong determinant in whether or not pursuing the given portfolio will produce significant returns. In other words, this return is crucial in measuring portfolio performance in the CAPM.
<p> The <i> Beta</i> ($\beta_{im}$) is a measure of the stock's volatility. More specifically, this component of the CAPM is a measure of the idiosyncratic or unsystematic risk. This is the risk that can be mitigated through investment diversification throughout a portfolio.
<br>
<h3>Beta value</h3>
<p>We get the Beta ($\beta$) value using the formula below:
    <p> $\large \beta = {Cov(r_{x},r_{m}) \over \sigma^{2}_{m}}$
        <br>
    <p>The Beta value indicates the relationship the investment has in relation to the market. In other words, this metric will show if an investment will or will not behave similarly to the rest of the market.
    <p> If $\beta = 0$, then the stock behaves indepdently of the market.
    <p> If $\beta < 1$, then the stock is <i>defensive</i> because they will lose less in poor markets - i.e. they are safe in poor markets.
    <p> If $\beta = 1$, then the stock performs the same as the market.
    <p> If $\beta > 1$, then the stock is <i>aggresive</i> because they are riskier investments BUT they perform better than the market.
<br>
<h2>The Sharpe Ratio</h2>
<p> The <i>Sharpe ratio</i> formula:
   <p> $\large {r_{i}-r_{f} \over\sigma_{i}}$
    <ul>
    <li> Risk-Free Return ($r_{f}$)
    <li> Return of the investment ($r_{i}$) 
    <li> Standard Deviation of the investment ($\sigma_{i}$)
    </ul>
<p>The Sharpe ratio is a metric used to calculate an investment or portfolio's risk-adjusted return. It also highlights any additional return that is gained after taking on the risk. 
<p>Considered simply, a higher Sharpe ratio or index indicates a better return <i> relative to the risk of the investment or the relationship of the investments in the portfolio</i>.

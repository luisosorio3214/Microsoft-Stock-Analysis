<h1 align="center">Microsoft Stock Analysis</h1>
<p align="center">
  <img src="Static\microsoft_office.avif" width="800" height="250" allow="autoplay">
</p>

<p>
  <img src="https://img.shields.io/badge/R_Studio-lightblue" title="R">
  <img src="https://img.shields.io/github/last-commit/luisosorio3214/Microsoft-Stock-Analysis">
  <img src="https://img.shields.io/github/repo-size/luisosorio3214/Microsoft-Stock-Analysis">
  <img src="https://img.shields.io/badge/Deep_Learning-orange">
  <img src="https://img.shields.io/badge/License-MIT-yellow">
  <a href="https://luisosorio3214.github.io/Machine-Learning-Project-R/Microsoft%20Stock%20Prediction%20-%20LSTM%20&%20GRU/"><img src="https://img.shields.io/badge/R_Notebook-green"></a>
  <a href="https://app.powerbi.com/view?r=eyJrIjoiYmQwNjkwYWQtY2ZmMy00NDBjLWIwMTYtZGE1ODI2MjhkM2QxIiwidCI6ImQxNzU2NzliLWFjZDMtNDY0NC1iZTgyLWFmMDQxOTgyOTc3YSIsImMiOjZ9"><img src="https://img.shields.io/badge/Power_BI-purple"></a>
  <a href="https://github.com/ellerbrock/open-source-badges/"><img src="https://badges.frapsoft.com/os/v1/open-source.svg?v=103"></a>

  <p>
    Badge <a href="https://shields.io/">Source</a>
  </p>
</p>

<p>
  <h2>Authors</h2>
  <ul>
    <li><a href="https://github.com/luisosorio3214">@luisosorio3214</a></li>
  </ul>
</p>

<p>
  <h2>Table of Contents</h2>
  <ul>
    <li><a href="#context" target="_parent">Context</a></li>
    <li><a href="#data-source">Data Source</a></li>
    <li><a href="#methods">Methods</a></li>
    <li><a href="#tech-stack">Tech Stack</a></li>
    <li><a href="#quick-glance">Quick glance at the Results</a></li>
    <li><a href="#lesson-learned">Lessons learned and Recommendation</a></li>
    <li><a href="#limitation">Limitation and what can be Improved</a></li>
    <li><a href="#markdown">R Markdown</a></li>
    <li><a href="#website">Website</a></li>
    <li><a href="#hub">Deployment on GitHub Pages</a></li>
    <li><a href="#deployed">Website Deployed</a></li>
    <li><a href="#contribution">Contribution</a></li>
    <li><a href="#license">License</a></li>
  </ul>
</p>


<P>
  <section id="context">
    <h2>Context</h2>
    <p>
      I like to study macro-economics and it is quite essential when reading stock market prices since they are heavily influenced by it. It is quite remarkable how a single statement from the Federal Reserve chairman, Jerome Powell and the entire stock price completely changes course. I usually spend time watching the Fed Minutes and also find interesting how several news outlets ask Jerome tricky questions to pull more information to expose hidden truths. The motivation for this particular project was to use Microsoft Stock prices and relate them to historical events that have impacted our economy to tell a compelling story about tech and economics. I also wanted to build some deep learning models to see if I can try to predict the movement of the stock price. 
    </p>
  </section>
</P>

<p>
  <section id="data-source">
    <h2>Data Source</h2>
    <ul>
      <li><a href="https://finance.yahoo.com/quote/MSFT/?fr=sycsrp_catchall" target="_blank">Yahoo Finance</a></li>
    </ul>
  </section>
</p>

<p>
  <section id="methods">
    <h2>Methods</h2>
    <ul>
      <li>Data Preprocessing</li>
      <li>Deep Learning Modeling</li>
      <li>Power BI</li>
      <li>App Deployment</li>
    </ul>
  </section>
</p>

<p>
  <section id="tech-stack">
    <h2>Tech Stack</h2>
    <ul>
      <li>R (Deep Learning modeling)</li>
      <li>Power BI (Dashboard creation)</li>
      <li>HTML/CSS (website)</li>
      <li>GitHub Pages (web app deployment)</li>
    </ul>
  </section>
</p>



<p>
  <section id="quick-glance">
    <h2>Quick Glance at Deep Learning Results</h2>
    <p>
      Long Short Term Memory - Prediction Plot 
      <p>
        <img src="Static\LSTM_plot.png">
      </p>
    </p>  
    <p>
      Gated Recurrent Unit - Predict Plot 
      <p>
        <img src="Static\GRU_Plot.png">
      </p>
    </p>
    <p>
      Deep Learning Algorithms Results
      <table style="width:100%">
        <tr>
          <th>Model</th>
          <th>Mean Absolute Error</th>
          <th>Mean Squared Error</th>
          <th>Root Mean Squared Error</th>
        </tr>
        <tr>
          <td>Long Short Term Memory (LSTM)</td>
          <td>15.46492</td>
          <td>314.6245</td>
          <td>17.73766</td>
        </tr>
        <tr>
          <td>Gated Recurrent Unit</td>
          <td>8.10126</td>
          <td>92.75793</td>
          <td>9.631092</td>
        </tr>
      </table>
      </p>
      <p>
        <ul>
          <li>Activation Function Used: tanh</li>
          <li>Loss Function: Mean Squared Error</li>
          <li>Metric Used: Mean Squared Error </li>
          <li>Best Model: Gated Recurrent Unit</li>
          <li>Why use Mean Squared Error: Observe that the goal of this project was for our deep learning model to predict the closing price of the stock for that day. We were dealing with a regression problem and metrics such as F1-Score, Recall, and accuracy do not make sense in this scenario. Now, Mean Squared Error value represents the average squared difference between the predicted values and the actual values. Since we are taking the average squared difference, MSE can never be negative and the lower the MSE the more indication that the model performed a better fit to the data. Now if we take the square root of the mean squared error, we get the root mean squared error which takes the same units of the actual data. In short hand, its similar in metric but it is more interpretable and easier to compare to the actual data. For example, we can say for GRU model which had the best mean squared error compared to the two had a root mean squared error of about 9.63 thus we can say on average the predicted price was about $9.63 away from the actual price. This where we can take standard deviation to make a confidence interval if we wanted to.</li>
        </ul>
      </p>
    </p>
  </section>
</p>

<p>
  <section id="lesson-learned">
  <h2>Lessons Learned and Recommendation</h2>
  <p>
    <ul>
      <li>The biggest lesson learned in this project was the difficulty in setting up a deep learning environment in R Studio. I did not know that it the end it uses python and same libraries such as tensorflow and keras. I would never work with deep learning models in R again since I already have working knowledge in python, my preferred programming language. However, R still reigns supreme when it comes down to statistical analysis and still conduct many of my hypothesis tests in R along some Linear/Logistic Regressions.</li> 
      <li>Another major lessons learned was to properly chose the number of epochs (steps to train the model) since we can potentially over fit the model. Over fitting the model would imply a low bias but high variance meaning our testing set predictions we be far off for our actual values. We want the perfect balance between bias and variance.
      <p><img src="Static\bias_variance.png" title="Bias-Variance">
          <img src="Static\overfitt.png" title="Overfit-Underfit"></p> </li>
    </ul>
  </p>
</p>

<P>
  <section id="limitation">
    <h2>Limitation and what can be Improved</h2>
    <p>
      <ul>
        <li>Now we tested the validity of our model using a testing set which was stored apart from the data in which our model was trained on. This provides us no new information since we already know the values of the testing set. Now Suppose we wanted to predict the closing price for a date in the future, then we simply create a data frame containing the date of the day and feed into our model giving us a value. Now stock prices are influence by a multitude of factors and no one can really predict a Black Swan Event which can heavily influence a price. For example, Covid caused many stocks to crash and no one expected a worldwide shut down because of it. Therefore, a deep learning model will never be able to fully predict a closing price. There's companies that take many factors into consideration and place them in their models such as tweets from influencer, market sentiment, and stock technical analysis.</li>
      </ul>
    </p>
  </section>
</p>

<p>
  <section id="markdown">
  <h2>R Markdown</h2>
  <p>
    To see the full R Markdown notebook click <a href="https://luisosorio3214.github.io/Machine-Learning-Project-R/Microsoft%20Stock%20Prediction%20-%20LSTM%20&%20GRU/" target="_blank">here</a>.
  </p>
  </section>
</p>

<p>
  <section id="website">
  <h2>Checkout the Website with dashboard</h2>
  <p>
    To read full Microsoft Stock Analysis with a story relating to tech and economics click <a href="https://luisosorio3214.github.io/Power-BI-Dashboards/Microsoft%20Stock/" target="_blank">here</a>.
  </p>
  </section>
</p>


<p>
  <section id="hub">
    <h2>Deployment using GitHub Pages</h2>
    <p>
      Did you know you can deploy a website for free using GitHub Pages? I will teach step by step on how to deploy your own website.
      <ol>
        <li>First Create a GitHub Repository</li>
        <li>Next build your website using your HTML code and name the file index.html. Note: You do not have to name the html file index however it will make it easier when directing to your site.</li>
        <li>Next, go to your repository settings. Go to Pages. </li>
        <li>Under the Branch title, where it says None click and choose the branch in which your repository is using. For most it will be the Main Branch.</li>
        </li>You can view the deployment process under the GitHub Actions. This is where you can customize your own build process which is a whole course in itself.</li>
        <li>After some time, you will see in the pages setting a link appear. This is the Website to your html file.</li>
      </ol>
    </p>
  </section>
</p>

<p>
  <section id="deployed">
  <h2>Website Deployed</h2>
  <img src="Static\stock_gif.gif">
  <p>
    Video to gif <a href="https://ezgif.com/">tool</a>
  </p>
  </section>
</p>

<p>
  <section id="contribution">
    <h2>Contribution</h2>
    <p>
      Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change or contribute.
    </p>
  </section>
</p>

<p>
  <section id="license">
    <h2>License</h2>
    <p>
      MIT License <br> <br>
      Copyright (c) 2022 Stern Semasuka <br> <br>
      Permission is hereby granted, free of charge, to any person obtaining a copy
      of this software and associated documentation files (the "Software"), to deal
      in the Software without restriction, including without limitation the rights
      to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
      copies of the Software, and to permit persons to whom the Software is
      furnished to do so, subject to the following conditions: <br> <br>
      The above copyright notice and this permission notice shall be included in all
      copies or substantial portions of the Software.<br> <br>
      THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
      IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
      FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
      AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
      LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
      OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
      SOFTWARE.<br> <br>
      Learn more about <a href="https://choosealicense.com/licenses/mit/" target="_blank"> MIT </a> license
    </p>
  </section>
</p>

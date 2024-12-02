# Datasets



## Table of Contents

1. [Overview](#Overview)

1. [Univariate time series](#Univariate-time-series)

1. [Multivariate time series](#Multivariate-time-series)

<!-- 1. [Dataset comprehensiveness](#Dataset-comprehensiveness) -->

   

## Overview


<style>       
.container {
        display: flex;
        width: 100%;
        max-width:100%;
        padding:0;
    }
    .text-section {
        /* flex: 3; */
        /* width:60%; */
        padding-right:50px;
        /* max-width:607px */
        width:500px;
    }
    .image-section {
        /* flex: 2.3; */
        text-align: center;
        width:675px;
    }
    .image-section img {
        max-width: 100%;
        height: auto;
        margin-top:8px;

    }
    .header {
        font-size: 3.5em;
        margin-bottom:3%
    }
    .section-title {
        font-weight: bold;
        display:inline;
    }
    .content {
      font-size: 1.2em;
      /* margin-bottom:3%; */
      margin-bottom:10px;
      width:100%;
      line-height:1.5
    }
    .link {
        color: blue;
        text-decoration: none;
    }
    .link:hover {
        text-decoration: underline;
    }
</style>
<div class="content">
            The Time series Forecasting Benchmark (TFB) aims to provide a wide variety of time series datasets that cover diverse charactistics, rich domains, multiple tasks, and varying lengths and dimensions.
        </div>
<div class="container">
    <div class="text-section">
        <!-- <div class="header">OGB Dataset Overview</div> -->
        <div class="content"> 
            <div class="section-title">Diverse charactistics: </div>
           TFB covers diverse time series data characteristics, including seasonality, trend, stationarity, transition, shifting, and correlation.
        </div>
        <div class="content">
          <div class="section-title">Rich domains: </div>
            TFB datasets come from ten different domains, including traffic, electricity, energy, the environment, nature, economic, stock markets, banking, health, and the web.
      </div>
    <div class="content">
        <div class="section-title">Multiple tasks: </div>
        We cover two fundamental time series forecasting tasks: <a href="#Univariate-time-series" class="link">univariate forecating</a> and <a href="#Multivariate-time-series" class="link">multivariate forecating</a>.
  </div>
    </div>
    <div class="image-section">
        <img src="../figures/Main-datasets-leaderboard.drawio.png">
    </div>

</div>


## Univariate time series

The univariate dataset includes 8,068 time series which are carefully curated from 16 open-source datasets from multiple domains. Table 1 categorizes the univariate dataset by sampling frequency; and for each frequency category, it reports the number of time series with different charactistics, including seasonality, trend, shifting, transition, stationarity, and the average lengths.  

<div style="display: flex;justify-content: center; /* 水平居中 */padding: 0;">
<table class="my-table" style="width: 90%;">
  <thead>
    <tr>
      <th>Frequency</th>
      <th>#Series</th>
      <th>Seasonality</th>
      <th>Trend</th>
      <th>Shifting</th>
      <th>Transition</th>
      <th>Stationarity</th>
      <th>Average Lens</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Yearly</td>
      <td>1,500</td>
      <td>611</td>
      <td>1,086</td>
      <td>978</td>
      <td>633</td>
      <td>354</td>
      <td>32</td>
    </tr>
    <tr>
      <td>Quarterly</td>
      <td>1,514</td>
      <td>486</td>
      <td>933</td>
      <td>889</td>
      <td>894</td>
      <td>471</td>
      <td>97</td>
    </tr>
    <tr>
      <td>Monthly</td>
      <td>1,674</td>
      <td>883</td>
      <td>884</td>
      <td>778</td>
      <td>1,212</td>
      <td>667</td>
      <td>259</td>
    </tr>
    <tr>
      <td>Weekly</td>
      <td>805</td>
      <td>253</td>
      <td>330</td>
      <td>445</td>
      <td>407</td>
      <td>372</td>
      <td>536</td>
    </tr>
    <tr>
      <td>Daily</td>
      <td>1,484</td>
      <td>374</td>
      <td>502</td>
      <td>487</td>
      <td>1,176</td>
      <td>714</td>
      <td>4,951</td>
    </tr>
    <tr>
      <td>Hourly</td>
      <td>706</td>
      <td>435</td>
      <td>276</td>
      <td>284</td>
      <td>680</td>
      <td>472</td>
      <td>5,109</td>
    </tr>
    <tr>
      <td>Other</td>
      <td>385</td>
      <td>75</td>
      <td>248</td>
      <td>236</td>
      <td>195</td>
      <td>124</td>
      <td>1,678</td>
    </tr>
    <tr>
      <td><i>Total</i></td>
      <td><i>8,068</i></td>
      <td><i>3,117</i></td>
      <td><i>4,259</i></td>
      <td><i>4,097</i></td>
      <td><i>5,197</i></td>
      <td><i>3,174</i></td>
      <td><i>1,569</i></td>
    </tr>
  </tbody>
</table>
</div>





<!-- ![](../figures/single-data.png) -->

<center style="font-size:14px;color:#C0C0C0;text-decoration:underline">Table 1: Statistics of univariate datasets.</center>

## Multivariate time series
The multivariate datasets include 25 multivariate time series from 10 domains. The sampling frequencies vary from every 5 minutes to 1 month, the range of feature dimensions varies from 5 to 2,000, and the time series length varies from 728 to 57,600. This substantial diversity of the multivariate datasets enables comprehensive benchmarking of different forecasting methods. To ensure fair comparisons, we choose a fixed data split ratio for each dataset chronologically, e.g., 7:1:2 or 6:2:2, for training, validation and testing. 
<style>
  /* 基本表格样式 */
  table.my-table {
    min-width: 100%;
    border-collapse: collapse;
    font-family: Arial, sans-serif;
    border: none; /* 去除表格边框 */

  }

  /* 表头样式 */
  table.my-table th {
    background-color: #f2f2f2; /* 表头背景色（奇数行浅灰色） */
    color: black; /* 表头文字颜色 */
    font-weight: bold; /* 表头字体加粗 */
    padding: 10px; /* 调整表头内边距 */
    text-align: center; /* 居中对齐 */
    border: none;
  }

  /* 偶数行背景色 */
  table.my-table tr:nth-child(odd) {
    background-color: #ffffff; /* 偶数行背景色（白色） */
  }

  /* 奇数行背景色 */
  table.my-table tr:nth-child(even) {
    background-color: #f2f2f2; /* 奇数行背景色（浅灰色） */
  }


  /* 单元格样式 */
  table.my-table td {
    padding: 10px; /* 调整单元格内边距 */
    text-align: center; /* 居中对齐 */
    border: none; /* 去除单元格边框 */
    white-space: nowrap; /* 防止文本换行 */
  }

</style>

<style>
  /* 基本表格样式 */
  table.my-table1 {
    border-collapse: collapse;
    font-family: Arial, sans-serif;
    border: none; /* 去除表格边框 */
    margin:0
  }

  /* 表头样式 */
  table.my-table1 th {
    background-color: #f2f2f2; /* 表头背景色（奇数行浅灰色） */
    color: black; /* 表头文字颜色 */
    font-weight: bold; /* 表头字体加粗 */
    padding: 10px; /* 调整表头内边距 */
    text-align: center; /* 居中对齐 */
    border: none;
  }

  /* 偶数行背景色 */
  table.my-table1 tr:nth-child(odd) {
    background-color: #ffffff; /* 偶数行背景色（白色） */
  }

  /* 奇数行背景色 */
  table.my-table1 tr:nth-child(even) {
    background-color: #f2f2f2; /* 奇数行背景色（浅灰色） */
  }


  /* 单元格样式 */
  table.my-table1 td {
    padding: 10px; /* 调整单元格内边距 */
    text-align: center; /* 居中对齐 */
    border: none; /* 去除单元格边框 */
    white-space: nowrap; /* 防止文本换行 */
  }
  table.my-table1 tr td:nth-child(7),table.my-table1 tr th:nth-child(7)   {
  /* max-width: 0px; 设置第4行单元格最大宽度 */
  text-align: left;
}

.table-container {
  width: 100%; /* Adjust width as needed */
  /* max-width: 100%; Ensure it doesn't exceed the container width */
  /* Adjust height as needed */
  overflow-x: auto; /* Enable horizontal scroll */
  margin:auto;
  overflow-y: hidden; /* Enable vertical scroll */
  display: flex;justify-content: LEFT;
}


</style>

<!-- ![](../figures/multi-datasets.png) -->
<div style="width:100%" class="table-container">
<table class="my-table1" style="">
  <thead>
    <tr>
      <th>Dataset</th>
      <th>Domain</th>
      <th>Frequency</th>
      <th>Lengths</th>
      <th>Dim</th>
      <th>Split</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="https://arxiv.org/abs/1707.01926">METR-LA</a></td>
      <td>Traffic</td>
      <td>5 mins</td>
      <td>34,272</td>
      <td>207</td>
      <td>7:1:2</td>
      <td title='>Traffic speed dataset collected from loopdetectors in the LA County road network'>Traffic speed dataset collected from loopdetectors in the LA County road network</td>
    </tr>
    <tr>
      <td><a href="https://arxiv.org/abs/1707.01926">PEMS-BAY</a></td>
      <td>Traffic</td>
      <td>5 mins</td>
      <td>52,116</td>
      <td>325</td>
      <td>7:1:2</td>
      <td title='Traffic speed dataset collected from the CalTrans PeMS'>Traffic speed dataset collected from the CalTrans PeMS</td>
    </tr>
    <tr>
      <td><a href="https://ojs.aaai.org/index.php/AAAI/article/view/5438">PEMS04</a></td>
      <td>Traffic</td>
      <td>5 mins</td>
      <td>16,992</td>
      <td>307</td>
      <td>6:2:2</td>
      <td title='Traffic flow time series collected from the CalTrans PeMS'>Traffic flow time series collected from the CalTrans PeMS</td>
    </tr>
    <tr>
      <td><a href="https://ojs.aaai.org/index.php/AAAI/article/view/5438">PEMS08</a></td>
      <td>Traffic</td>
      <td>5 mins</td>
      <td>17,856</td>
      <td>170</td>
      <td>6:2:2</td>
      <td title='Traffic flow time series collected from the CalTrans PeMS'>Traffic flow time series collected from the CalTrans PeMS</td>
    </tr>
    <tr>
      <td><a href="https://proceedings.neurips.cc/paper/2021/hash/bcc0d400288793e8bdcd7c19a8ac0c2b-Abstract.html">Traffic</a></td>
      <td>Traffic</td>
      <td>1 hour</td>
      <td>17,544</td>
      <td>862</td>
      <td>7:1:2</td>
      <td title='Road occupancy rates measured by 862 sensors on San Francisco Bay area freeways'>Road occupancy rates measured by 862 sensors on San Francisco Bay area freeways</td>
    </tr>
    <tr>
      <td><a href="https://ojs.aaai.org/index.php/AAAI/article/view/17325">ETTh1</a></td>
      <td>Electricity</td>
      <td>1 hour</td>
      <td>14,400</td>
      <td>7</td>
      <td>6:2:2</td>
      <td title='Power transformer 1, comprising seven indicators such as oil temperature and useful load'>Power transformer 1, comprising seven indicators such as oil temperature and useful load</td>
    </tr>
    <tr>
      <td><a href="https://ojs.aaai.org/index.php/AAAI/article/view/17325">ETTh2</a></td>
      <td>Electricity</td>
      <td>1 hour</td>
      <td>14,400</td>
      <td>7</td>
      <td>6:2:2</td>
      <td title='Power transformer 2, comprising seven indicators such as oil temperature and useful load'>Power transformer 2, comprising seven indicators such as oil temperature and useful load</td>
    </tr>
    <tr>
      <td><a href="https://ojs.aaai.org/index.php/AAAI/article/view/17325">ETTm1</a></td>
      <td>Electricity</td>
      <td>15 mins</td>
      <td>57,600</td>
      <td>7</td>
      <td>6:2:2</td>
      <td title='Power transformer 1, comprising seven indicators such as oil temperature and useful load'>Power transformer 1, comprising seven indicators such as oil temperature and useful load</td>
    </tr>
    <tr>
      <td><a href="https://ojs.aaai.org/index.php/AAAI/article/view/17325">ETTm2</a></td>
      <td>Electricity</td>
      <td>15 mins</td>
      <td>57,600</td>
      <td>7</td>
      <td>6:2:2</td>
      <td title='Power transformer 2, comprising seven indicators such as oil temperature and useful load'>Power transformer 2, comprising seven indicators such as oil temperature and useful load</td>
    </tr>
    <tr>
      <td><a href="https://ergodicity.net/2013/07/">Electricity</a></td>
      <td>Electricity</td>
      <td>1 hour</td>
      <td>26,304</td>
      <td>321</td>
      <td>7:1:2</td>
      <td title='Electricity records the electricity consumption in kWh every 1 hour from 2012 to 2014'>Electricity records the electricity consumption in kWh every 1 hour from 2012 to 2014</td>
    </tr>
    <tr>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3209978.3210006">Solar</a></td>
      <td>Energy</td>
      <td>10 mins</td>
      <td>52,560</td>
      <td>137</td>
      <td>6:2:2</td>
       <td title='Solar production records collected from 137 PV plants in Alabama'>Solar production records collected from 137 PV plants in Alabama</td>
    </tr>
    <tr>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3209978.3210006">Wind</a></td>
      <td>Energy</td>
      <td>15 mins</td>
      <td>48,673</td>
      <td>7</td>
      <td>7:1:2</td>
      <td title='Wind power records from 2020-2021 at 15-minute intervals'>Wind power records from 2020-2021 at 15-minute intervals</td>
    </tr>
    <tr>
      <td><a href="https://proceedings.neurips.cc/paper/2021/hash/bcc0d400288793e8bdcd7c19a8ac0c2b-Abstract.html">Weather</a></td>
      <td>Environment</td>
      <td>10 mins</td>
      <td>52,696</td>
      <td>21</td>
      <td>7:1:2</td>
      <td title='Recorded every for the whole year 2020, which contains 21 meteorological indicators'>Recorded every for the whole year 2020, which contains 21 meteorological indicators</td>
    </tr>
    <tr>
      <td><a href="https://royalsocietypublishing.org/doi/abs/10.1098/rspa.2017.0457">AQShunyi</a></td>
      <td>Environment</td>
      <td>1 hour</td>
      <td>35,064</td>
      <td>11</td>
      <td>6:2:2</td>
      <td title='Air quality datasets from a measurement station, over a period of 4 years'>Air quality datasets from a measurement station, over a period of 4 years</td>
    </tr>
    <tr>
      <td><a href="https://royalsocietypublishing.org/doi/abs/10.1098/rspa.2017.0457">AQWan</a></td>
      <td>Environment</td>
      <td>1 hour</td>
      <td>35,064</td>
      <td>11</td>
      <td>6:2:2</td>
      <td title='Air quality datasets from a measurement station, over a period of 4 years'>Air quality datasets from a measurement station, over a period of 4 years</td>
    </tr>
    <tr>
      <td><a href="https://academic.oup.com/treephys/article-abstract/36/12/1449/2571314">ZafNoo</a></td>
      <td>Nature</td>
      <td>30 mins</td>
      <td>19,225</td>
      <td>11</td>
      <td>7:1:2</td>
      <td title='From the Sapflux data project includes sap flow measurements and nvironmental variables'>From the Sapflux data project includes sap flow measurements and nvironmental variables</td>
    </tr>
    <tr>
      <td><a href="https://academic.oup.com/treephys/article-abstract/36/12/1449/2571314">CzeLan</a></td>
      <td>Nature</td>
      <td>30 mins</td>
      <td>19,934</td>
      <td>11</td>
      <td>7:1:2</td>
      <td title='From the Sapflux data project includes sap flow measurements and nvironmental variables'>From the Sapflux data project includes sap flow measurements and nvironmental variables</td>
    </tr>
    <tr>
      <td><a href="https://www.tandfonline.com/doi/abs/10.1080/07350015.2015.1086655">FRED-MD</a></td>
      <td>Economic</td>
      <td>1 month</td>
      <td>728</td>
      <td>107</td>
      <td>7:1:2</td>
      <td title='Time series showing a set of macroeconomic indicators from the Federal Reserve Bank'>Time series showing a set of macroeconomic indicators from the Federal Reserve Bank</td>
    </tr>
    <tr>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3209978.3210006">Exchange</a></td>
      <td>Economic</td>
      <td>1 day</td>
      <td>7,588</td>
      <td>8</td>
      <td>7:1:2</td>
      <td title='ExchangeRate collects the daily exchange rates of eight countries'>ExchangeRate collects the daily exchange rates of eight countries</td>
    </tr>
    <tr>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3309547">NASDAQ</a></td>
      <td>Stock</td>
      <td>1 day</td>
      <td>1,244</td>
      <td>5</td>
      <td>7:1:2</td>
      <td title='Records opening price, closing price, trading volume, lowest price, and highest price'>Records opening price, closing price, trading volume, lowest price, and highest price</td>
    </tr>
    <tr>
      <td><a href="https://dl.acm.org/doi/abs/10.1145/3309547">NYSE</a></td>
      <td>Stock</td>
      <td>1 day</td>
      <td>1,243</td>
      <td>5</td>
      <td>7:1:2</td>
      <td title='Records opening price, closing price, trading volume, lowest price, and highest price'>Records opening price, closing price, trading volume, lowest price, and highest price</td>
    </tr>
    <tr>
      <td><a href="https://www.sciencedirect.com/science/article/pii/S0957417412000528">NN5</a></td>
      <td>Banking</td>
      <td>1 day</td>
      <td>791</td>
      <td>111</td>
      <td>7:1:2</td>
      <td title='NN5 is from banking, records the daily cash withdrawals from ATMs in UK'>NN5 is from banking, records the daily cash withdrawals from ATMs in UK</td>
    </tr>
    <tr>
      <td><a href="https://proceedings.neurips.cc/paper/2021/hash/bcc0d400288793e8bdcd7c19a8ac0c2b-Abstract.html">ILI</a></td>
      <td>Health</td>
      <td>1 week</td>
      <td>966</td>
      <td>7</td>
      <td>7:1:2</td>
      <td title='Recorded indicators of patients data from Centers for Disease Control and Prevention'>Recorded indicators of patients data from Centers for Disease Control and Prevention</td>
    </tr>
    <tr>
      <td><a href="https://ojs.aaai.org/index.php/AAAI/article/view/16616">Covid-19</a></td>
      <td>Health</td>
      <td>1 day</td>
      <td>1,392</td>
      <td>948</td>
      <td>7:1:2</td>
      <td title="Provide opportunities for researchers to investigate the dynamics of COVID-19">Provide opportunities for researchers to investigate the dynamics of COVID-19</td>
    </tr>
    <tr>
      <td><a href="https://proceedings.mlr.press/v89/gasthaus19a.html">Wike2000</a></td>
      <td>Web</td>
      <td>1 day</td>
      <td>792</td>
      <td>2,000</td>
      <td>7:1:2</td>
      <td  title="Wike2000 is daily page views of 2000 Wikipedia pages">Wike2000 is daily page views of 2000 Wikipedia pages</td>
    </tr>
  </tbody>
</table>
</div>


<center style="font-size:14px;color:#C0C0C0;text-decoration:underline">Table 2: Statistics of multivariate datasets.</center>


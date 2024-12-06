# Leaderboards

<style>
  /* 基本表格样式 */
  table.my-table2 {
    width: 100%;
    border-collapse: collapse;
    font-family: Arial, sans-serif;
    border: none; /* 去除表格边框 */
    padding: 0;
    margin: 0;
  }

  /* 表头样式 */
  table.my-table2 th {
    background-color: #f2f2f2; /* 表头背景色（奇数行浅灰色） */
    color: black; /* 表头文字颜色 */
    font-weight: bold; /* 表头字体加粗 */
    padding: 10px; /* 调整表头内边距 */
    text-align: center; /* 居中对齐 */
    white-space: nowrap; /* 防止文本换行 */
    border: none;
  }

  /* 偶数行背景色 */
  table.my-table2 tr:nth-child(odd) {
    background-color: #ffffff; /* 偶数行背景色（白色） */
  }

  /* 奇数行背景色 */
  table.my-table2 tr:nth-child(even) {
    background-color: #f2f2f2; /* 奇数行背景色（浅灰色） */
  }

  /* 单元格样式 */
  table.my-table2 td {
    padding: 8px; /* 调整单元格内边距 */
    text-align: center; /* 居中对齐 */
    border: none; /* 去除单元格边框 */
    vertical-align: middle;
    /* white-space: nowrap; 防止文本换行 */
    /* overflow: hidden; 隐藏溢出内容
    text-overflow: ellipsis; 溢出内容显示省略号 */
    /* max-width: 200px; 设置单元格最大宽度
    position: relative; 设置相对定位以显示悬停内容 */
  }

  /* 第4列单独样式 */
  table.my-table2 tr td:nth-child(4) {
    /* max-width: 150px; 设置第4列单元格最大宽度 */
  }

  /* 第2列单独样式 */
  table.my-table2 tr td:nth-child(2) {
    /* max-width: 80px; 设置第2列单元格最大宽度 */
  }

  /* 第7列单独样式 */
  table.my-table2 tr td:nth-child(7) {
    /* max-width: 100px; 设置第7列单元格最大宽度 */
  }
  .table-container {
    width: 100%; /* Adjust width as needed */
    max-width: 100%; /* Ensure it doesn't exceed the container width */
    /* Adjust height as needed */
    overflow-x: auto; /* Enable horizontal scroll */
    overflow-y: hidden; /* Enable vertical scroll */
    padding-left: 0px;
  }
  .table-container {
    width: 80%; /* Adjust width as needed */
    /* max-width: 100%; Ensure it doesn't exceed the container width */
    /* Adjust height as needed */
    overflow-x: auto; /* Enable horizontal scroll */
    margin: auto;
    overflow-y: hidden; /* Enable vertical scroll */
    display: flex;
    justify-content: LEFT;
  }
  select {
    background-color: #f2f2f2; /* 表头背景色（奇数行浅灰色） */
    color: black; /* 表头文字颜色 */
    font-weight: bold; /* 表头字体加粗 */
    text-align: center; /* 居中对齐 */
    white-space: nowrap; /* 防止文本换行 */
    border: none;
    margin: auto;
  }
  select:focus {
    border: none; /* 确保选中时没有边框 */
    outline: none; /* 确保选中时没有黑框 */
  }
  option {
    padding: 5px, 0;
  }
  .checkbox-item {
    margin-left: 10px;
  }

  .main-container {
    display: flex;
    align-items: stretch; /* Stretch items to the same height */
    height: 100%;
  }
  .checkbox-container1 {
    display: grid;
    grid-template-columns: 1fr; /* 分为两列 */
    gap: 10px;
    padding-right: 20px; /* Add some space between checkboxes and table */
    overflow-y: auto; /* Enable vertical scroll if needed */
  }
  .checkbox-container {
    /* display: grid; */
    grid-template-columns: 0.7fr 0.7fr; 分为两列
    padding-right: 10px; /* Add some space between checkboxes and table */
    overflow-y: auto; /* Enable vertical scroll if needed */
  }
  .category h3 {
    display: flex;
    align-items: center;
  }

  .category {
    margin-bottom: 10px;
  }
  .checkbox-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    height: 100%;
    width: fit-content;
  }
  .article-entry h3 {
    margin: 0;
    margin-right: 6px;
  }
  .all-checkbox {
    display: flex;
    align-items: center;
    margin-bottom: 10px; /* 在 "All" 复选框和其他复选框之间添加一些间距 */
  }
  .checkbox-wrapper-metrics{
    display: grid;
    grid-template-columns: 1fr 1fr; /* 设置为两列 */
    gap: 0;
    width: 250px; /* 根据需要调整宽度 */
  }
  .checkbox-wrapper1 {
    display: grid;
    grid-template-columns: 1fr;
    width: 250px;
  }

  .checkbox-wrapper2 {
    display: grid;
    grid-template-columns: 1.5fr 1.5fr 1.5fr 1.5fr;
    width: 260px;
  }
  .checkbox-wrapper3 {
    display: grid;
    grid-template-columns: 1;
    width: 100%;
  }
  .checkbox-wrapper3 .checkbox-item {
    margin-left: 15px;
    margin-top: 10px;
  }
  .category h3 {
    display: flex;
    align-items: baseline;
  }
  input[type='number'] {
    border: none; /* 去掉边框 */
    border-bottom: 1px solid #000; /* 底部添加一条横线 */
    outline: none;
    padding: 0px;
    /* padding-right: 0px;  */

    width: 31px;
    font-size: 14px;
    /* text-align:right; */
    text-align: center;
  }
  input::-webkit-outer-spin-button,
  input::-webkit-inner-spin-button {
    -webkit-appearance: none;
  }
  input[type='number'] {
    -moz-appearance: textfield;
  }

  .sticky-col {
    background-color: white;
    position: sticky;
    left: 0; /* 固定在左侧 */
    z-index: 1; /* 设定堆叠顺序 */
    /* box-shadow: rgba(0, 0, 0, 0.4) -2px 0px 3px -1px; */
  }
  /* 确保交叉单元格的堆叠顺序 */
  .sticky-col-header {
    z-index: 3;
  }
  .sticky-th {
    position: sticky;
    top: 0; /* 固定在顶部 */
    z-index: 2; /* 设定堆叠顺序 */
  }
  .double-underline {
    position: relative;
    display: inline-block;
    /* font: inherit; 继承父元素的字体样式 */
  }
  .double-underline::after,
  .double-underline::before {
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    height: 1px; /* 下划线的厚度 */
    background-color: black; /* 下划线的颜色 */
  }
  .double-underline::before {
    bottom: 3px; /* 第一条下划线的位置 */
  }
  .double-underline::after {
    bottom: 0px; /* 第二条下划线的位置 */
  }
  .sticky-col2 {
    position: sticky;
    left: 36px; /* 根据第一列的宽度设置 */
    z-index: 1;
    background-color: #fff;
  }
  .sticky-col2::after {
    content: '';
    position: absolute;
    top: 0;
    right: 0px; /* 调整阴影位置 */
    width: 5px;
    height: 105%;
    box-shadow: 2px 0 3px -2px rgba(0, 0, 0, 0.4); /* 右侧阴影 */
  }
</style>

## Leaderboard for multivariate time series forecasting

<div class="main-container" id="main-container-full">
  <div class="checkbox-wrapper">
    <div class="checkbox-container" id="dataset-container-mul-type-full">
      <div class="category" style="margin-bottom:0px;width: 300px;">
        <h3>
          <input type="checkbox" id="select-all-type-full" style='display:none' onchange="toggleCategory('Type','full', this.checked)">
          Learning Paradigm
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Type','full', true)" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleCategory('Type','full', false)" style="padding:0 3px">off</a>]</b>
        </h3>
        <div class="checkbox-wrapper1">
          <div class="checkbox-item">
            <input type="checkbox" id="Type-full/Non-Learning-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-full">
            <label for="Type-full/Non-Learning-Model">Non-Learning</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Type-full/Machine-Learning-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-full">
            <label for="Type-full/Machine-Learning-Model" >Machine-Learning</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Type-full/Deep-Learning-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-full">
            <label for="Type-full/Deep-Learning-Model">Deep-Learning</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Type-full/LLM-Based-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-full">
            <label for="Type-full/LLM-Based-Model">LLM-Based</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Type-full/Pre-trained-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-full">
            <label for="Type-full/Pre-trained-Model">TS Pre-trained</label>
          </div>
        </div>
      </div>
    </div>
     <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div class="checkbox-container" id="dataset-container-mul-up-full">
      <div class="category" style="margin-bottom:0px">
        <h3>
          <input type="checkbox" id="select-all-Metrics-full" style='display:none' onchange="toggleCategory('Metrics','full', this.checked)">
          Metrics
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Metrics','full', true)" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleCategory('Metrics','full', false)" style="padding:0 3px">off</a>]</b>
        </h3>
        <div class="checkbox-wrapper-metrics">
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/A-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/A-P">A-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/A-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/A-R">A-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/Acc" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/Acc">Acc</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/Aff-F1" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/Aff-F1">Aff-F1</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/Aff-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/Aff-P">Aff-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/Aff-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/Aff-R">Aff-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/F1" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/F1">F1</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/P">P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/R">R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/R-A-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/R-A-P">R-A-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/R-A-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/R-A-R">R-A-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/R-F1" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/R-F1">R-F1</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/R-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/R-P">R-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/R-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/R-R">R-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/V-PR" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/V-PR">V-PR</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-full/V-ROC" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-full">
            <label for="Metrics-full/V-ROC">V-ROC</label>
          </div>
        </div>
      </div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div id='all-full'>
      <div class='checkbox-container'>
        <div class="all-checkbox">
          <!-- <input type="checkbox" id="select-all" onclick="toggleSelectAll(this.checked,'full')" style="display:none"> -->
          <label for="select-all">
            <h3 style="white-space:nowrap">Datasets
              <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleSelectAll(true,'full')" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleSelectAll(false,'full')" style="padding:0 3px">off</a>]</b>
            </h3>
          </label>
        </div>
      </div>
      <div class="checkbox-container" id="dataset-container-full"></div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <!-- Forecasting Horizons -->
    <!-- <div class="checkbox-container1" id="dataset-container-mul-down">
      <div class="category" style="margin-bottom:0px">
        <h3>
          <input type="checkbox" id="select-all-Horizons-full" style='display:none' onchange="toggleCategory('Horizons', this.checked)">
          Forecasting Horizons
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Horizons','full', true)" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleCategory('Horizons','full', false)" style="padding:0 3px">off</a>]</b>
        </h3>
        <div class="checkbox-wrapper2">
          <div class="checkbox-item">
            <input type="checkbox" id="Horizons-full/96" onchange="handleChildCheckboxChange(event)" class="checkbox-Horizons-full">
            <label for="Horizons/96">96</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Horizons-full/192" onchange="handleChildCheckboxChange(event)" class="checkbox-Horizons-full">
            <label for="Horizons/192">192</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Horizons-full/336" onchange="handleChildCheckboxChange(event)" class="checkbox-Horizons-full">
            <label for="Horizons/336">336</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Horizons-full/720" onchange="handleChildCheckboxChange(event)" class="checkbox-Horizons-full">
            <label for="Horizons/720">720</label>
          </div>
        </div>
      </div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div> -->
    <div class="checkbox-container1" id="dataset-container-mul-down1">
      <div class="category" style="margin-bottom:0px">
        <h3>
          <input type="checkbox" id="select-all-Score-full" style='display:none' onchange="toggleCategory('Score','full', this.checked)">
          Score
        </h3>
        <div class="checkbox-wrapper3">
          <div class="checkbox-item">
            <input type="radio" id="Score-full/1" value="Score/1" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-full">
            <label for="Score/1">🥇</label>
          </div>
          <div class="checkbox-item">
            <input type="radio" id="Score-full/2" value="Score/2" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-full">
            <label for="Score/2">🥇 + 🥈 + 🥉</label>
          </div>
          <div class="checkbox-item" style="flex-wrap:nowrap;">
            <input type="radio" id="Score-full/3" value="Score/3" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-full">
            <label for="Score/3">
            <input type="number" id="score-full/3/1" name="score/3/1" value="3" oninput="validateInput(this)"> × 🥇 + 
            <input type="number" id="score-full/3/2" name="score/3/2" value="2" oninput="validateInput(this)"> × 🥈 + 
            <input type="number" id="score-full/3/3" name="score/3/3" value="1" oninput="validateInput(this)"> × 🥉</label>
          </div>
        </div>
      </div>
      <div style="height:5px"></div>
    </div>
  </div>
  <div style="width:100%;margin-top: 0;" class="table-container" id='table-container-mul'>
    <table id="full" class="my-table2">
      <thead>
        <tr>
          <th>Rank</th>
          <th>Model</th>
          <!-- <th>Parameters</th> -->
          <th>Score</th>
          <th>🥇</th>
          <th>🥈</th>
          <th>🥉</th>
          <th>Paper</th>
          <th>Publication</th>
          <th>Year</th>
        </tr>
      </thead>
      <tbody>
      </tbody>
    </table>
  </div>
</div>

### Rules:

- For multivariate forecasting algorithms, we consider 25 datasets and 2 error metrics, i.e., MAE and MSE. For each dataset, we consider 4 forecasting horizons. This gives 200 (25 * 4 * 2) unique evaluation settings ([click here](../200seetings) for details), [click here](./#Multivariate-forecasting-results) to see the detailed results, [click here](./MTSF_RESULTS.csv) to download detailed evaluation results for each of the 25 multivariate time series.

- For each forecasting algorithm, we count the number of times that the algorithm receives the gold, silver, and bronze medals, i.e., having the lowest, 2nd lowest, and 3rd lowest errors, shown as 🥇, 🥈, and 🥉, respectively.

- We provide three different types of scores for ranking the forecasting algorithms. First, the scores equal to the numbers of gold medals. Second, the scores are the sum of the numbers of gold, silver, and bronze medals. Third, the scores are the weighted sum of the gold, silver, and bronze medals, where the weights can be customized. The larger the score, the higher the ranking.
- Profile1 refers to a subset of ten datasets commonly used in recent literature, including Electricity, ETTm1, ETTm2, ETTh1, ETTh2, Traffic, Solar, Weather, ILI, and Exchange.

<div style="height:30px"></div>

<!-- ### Multivariate forecasting results -->

<div style="height:10px"></div>

<style>
  .sticky-col {
    background-color: white;
    position: sticky;
    left: 0; /* 固定在左侧 */
    z-index: 1; /* 设定堆叠顺序 */
    /* box-shadow: rgba(0, 0, 0, 0.4) -2px 0px 3px -1px; */
  }
  /* 确保交叉单元格的堆叠顺序 */
  .sticky-col-header {
    z-index: 3;
  }
  .sticky-th {
    position: sticky;
    top: 0; /* 固定在顶部 */
    z-index: 2; /* 设定堆叠顺序 */
  }
  .double-underline {
    position: relative;
    display: inline-block;
    /* font: inherit; 继承父元素的字体样式 */
  }
  .double-underline::after,
  .double-underline::before {
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    height: 1px; /* 下划线的厚度 */
    background-color: black; /* 下划线的颜色 */
  }
  .double-underline::before {
    bottom: 3px; /* 第一条下划线的位置 */
  }
  .double-underline::after {
    bottom: 0px; /* 第二条下划线的位置 */
  }
  .sticky-col2 {
    position: sticky;
    left: 36px; /* 根据第一列的宽度设置 */
    z-index: 1;
    background-color: #fff;
  }
  .sticky-col2::after {
    content: '';
    position: absolute;
    top: 0;
    right: 0px; /* 调整阴影位置 */
    width: 5px;
    height: 105%;
    box-shadow: 2px 0 3px -2px rgba(0, 0, 0, 0.4); /* 右侧阴影 */
  }
</style>

<div class="main-container">
  <div style="width:100%;overflow-y:auto;height:800px" class="table-container">
    <table id="multivariateTable211" class="my-table2">
      <thead>
      </thead>
      <tbody>
      </tbody>
    </table>
  </div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/PapaParse/5.3.0/papaparse.min.js"></script>
<script src='./modelMetricsDashboard.js'></script>

<script>
  loadDataAndInitializeSettings(['full'])
</script>

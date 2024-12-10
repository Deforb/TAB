# Leaderboards

## Leaderboard for univariate

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
    display: grid;
    grid-template-columns: 0.6fr 0.8fr; /* 分为两列 */
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
    /* margin-right: 6px; */
  }
  .all-checkbox {
    display: flex;
    align-items: center;
    margin-bottom: 10px; /* 在 "All" 复选框和其他复选框之间添加一些间距 */
  }
  .checkbox-wrapper-metrics{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr; /* 设置为两列 */
    gap: 0;
    width: 300px; /* 根据需要调整宽度 */
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

<div class="main-container" id="main-container-uni">
  <div class="checkbox-wrapper">
    <div class="checkbox-container" id="dataset-container-mul-type-uni">
      <div class="category" style="margin-bottom:0px;width: 300px;">
        <h3>
          <input type="checkbox" id="select-all-type-uni" style='display:none' onchange="toggleCategory('Type','uni', this.checked)">
          Learning Paradigm
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Type','uni', true)" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleCategory('Type','uni', false)" style="padding:0 3px">off</a>]</b>
        </h3>
        <div class="checkbox-wrapper1">
          <!-- <div class="checkbox-item">
            <input type="checkbox" id="Type-uni/Non-Learning-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-uni">
            <label for="Type-uni/Non-Learning-Model">Non-Learning</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Type-uni/Machine-Learning-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-uni">
            <label for="Type-uni/Machine-Learning-Model" >Machine-Learning</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Type-uni/Deep-Learning-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-uni">
            <label for="Type-uni/Deep-Learning-Model">Deep-Learning</label>
          </div> -->
          <div class="checkbox-item">
            <input type="checkbox" id="Type-uni/LLM-Based-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-uni">
            <label for="Type-uni/LLM-Based-Model">LLM-Based</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Type-uni/Pre-trained-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-uni">
            <label for="Type-uni/Pre-trained-Model">TS Pre-trained</label>
          </div>
        </div>
      </div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div class="checkbox-container" id="dataset-container-mul-strategy-uni">
      <div class="category" style="margin-bottom:0px;width: 300px;">
        <h3>
          <input type="checkbox" id="select-all-strategy-uni" style='display:none' onchange="toggleCategory('Strategy','uni', this.checked)">
          Evaluation strategies
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Strategy','uni', true)" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleCategory('Strategy','uni', false)" style="padding:0 3px">off</a>]</b>
        </h3>
        <div class="checkbox-wrapper1">
          <div class="checkbox-item">
            <input type="checkbox" id="Strategy-uni/zero" onchange="handleChildCheckboxChange(event)" class="checkbox-Strategy-uni">
            <label for="Strategy-uni/zero">Zero</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Strategy-uni/few" onchange="handleChildCheckboxChange(event)" class="checkbox-Strategy-uni">
            <label for="Strategy-uni/few">Few</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Strategy-uni/full" onchange="handleChildCheckboxChange(event)" class="checkbox-Strategy-uni">
            <label for="Strategy-uni/full">Full</label>
          </div>
        </div>
      </div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div class="checkbox-container" id="dataset-container-mul-up-uni">
      <div class="category" style="margin-bottom:0px">
        <h3>
          <input type="checkbox" id="select-all-Metrics-uni" style='display:none' onchange="toggleCategory('Metrics','uni', this.checked)">
          Metrics
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Metrics','uni', true)" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleCategory('Metrics','uni', false)" style="padding:0 3px">off</a>]</b>
        </h3>
        <div class="checkbox-wrapper-metrics">
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/A-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/A-P">A-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/A-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/A-R">A-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/Acc" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/Acc">Acc</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/Aff-F1" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/Aff-F1">Aff-F1</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/Aff-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/Aff-P">Aff-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/Aff-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/Aff-R">Aff-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/F1" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/F1">F1</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/P">P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/R">R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/R-A-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/R-A-P">R-A-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/R-A-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/R-A-R">R-A-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/R-F1" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/R-F1">R-F1</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/R-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/R-P">R-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/R-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/R-R">R-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/V-PR" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/V-PR">V-PR</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-uni/V-ROC" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-uni">
            <label for="Metrics-uni/V-ROC">V-ROC</label>
          </div>
        </div>
      </div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div id='all-uni'>
      <div class='checkbox-container'>
        <div class="all-checkbox">
          <label for="select-all">
            <h3 style="white-space:nowrap">Datasets
              <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleSelectAll(true,'uni')" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleSelectAll(false,'uni')" style="padding:0 3px">off</a>]</b>
            </h3>
          </label>
        </div>
      </div>
      <div class="checkbox-container" id="dataset-container-uni"></div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div class="checkbox-container1" id="dataset-container-mul-down1">
      <div class="category" style="margin-bottom:0px">
        <h3>
          <input type="checkbox" id="select-all-Score-uni" style='display:none' onchange="toggleCategory('Score','uni', this.checked)">
          Score
        </h3>
        <div class="checkbox-wrapper3">
          <div class="checkbox-item">
            <input type="radio" id="Score-uni/1" value="Score/1" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-uni">
            <label for="Score/1">🥇</label>
          </div>
          <div class="checkbox-item">
            <input type="radio" id="Score-uni/2" value="Score/2" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-uni">
            <label for="Score/2">🥇 + 🥈 + 🥉</label>
          </div>
          <div class="checkbox-item" style="flex-wrap:nowrap;">
            <input type="radio" id="Score-uni/3" value="Score/3" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-uni">
            <label for="Score/3">
            <input type="number" id="score-uni/3/1" name="score/3/1" value="3" oninput="validateInput(this)"> × 🥇 + 
            <input type="number" id="score-uni/3/2" name="score/3/2" value="2" oninput="validateInput(this)"> × 🥈 + 
            <input type="number" id="score-uni/3/3" name="score/3/3" value="1" oninput="validateInput(this)"> × 🥉</label>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div style="width:100%;margin-top: 0;" class="table-container" id='table-container-mul'>
    <table id="uni" class="my-table2">
      <thead>
        <tr>
          <th>Rank</th>
          <th>Model</th>
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

## Leaderboard for multivariate

<div class="main-container" id="main-container-multi">
  <div class="checkbox-wrapper">
    <div class="checkbox-container" id="dataset-container-mul-type-multi">
      <div class="category" style="margin-bottom:0px;width: 300px;">
        <h3>
          <input type="checkbox" id="select-all-type-multi" style='display:none' onchange="toggleCategory('Type','multi', this.checked)">
          Learning Paradigm
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Type','multi', true)" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleCategory('Type','multi', false)" style="padding:0 3px">off</a>]</b>
        </h3>
        <div class="checkbox-wrapper1">
          <div class="checkbox-item">
            <input type="checkbox" id="Type-multi/LLM-Based-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-multi">
            <label for="Type-multi/LLM-Based-Model">LLM-Based</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Type-multi/Pre-trained-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-multi">
            <label for="Type-multi/Pre-trained-Model">TS Pre-trained</label>
          </div>
        </div>
      </div>
    </div>
     <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
        <div class="checkbox-container" id="dataset-container-mul-strategy-multi">
      <div class="category" style="margin-bottom:0px;width: 300px;">
        <h3>
          <input type="checkbox" id="select-all-strategy-multi" style='display:none' onchange="toggleCategory('Strategy','multi', this.checked)">
          Evaluation strategies
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Strategy','multi', true)" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleCategory('Strategy','multi', false)" style="padding:0 3px">off</a>]</b>
        </h3>
        <div class="checkbox-wrapper1">
          <div class="checkbox-item">
            <input type="checkbox" id="Strategy-multi/zero" onchange="handleChildCheckboxChange(event)" class="checkbox-Strategy-multi">
            <label for="Strategy-multi/zero">Zero</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Strategy-multi/few" onchange="handleChildCheckboxChange(event)" class="checkbox-Strategy-multi">
            <label for="Strategy-multi/few">Few</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Strategy-multi/full" onchange="handleChildCheckboxChange(event)" class="checkbox-Strategy-multi">
            <label for="Strategy-multi/full">Full</label>
          </div>
        </div>
      </div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div class="checkbox-container" id="dataset-container-mul-up-multi">
      <div class="category" style="margin-bottom:0px">
        <h3>
          <input type="checkbox" id="select-all-Metrics-multi" style='display:none' onchange="toggleCategory('Metrics','multi', this.checked)">
          Metrics
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Metrics','multi', true)" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleCategory('Metrics','multi', false)" style="padding:0 3px">off</a>]</b>
        </h3>
        <div class="checkbox-wrapper-metrics">
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/A-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/A-P">A-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/A-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/A-R">A-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/Acc" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/Acc">Acc</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/Aff-F1" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/Aff-F1">Aff-F1</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/Aff-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/Aff-P">Aff-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/Aff-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/Aff-R">Aff-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/F1" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/F1">F1</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/P">P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/R">R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/R-A-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/R-A-P">R-A-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/R-A-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/R-A-R">R-A-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/R-F1" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/R-F1">R-F1</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/R-P" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/R-P">R-P</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/R-R" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/R-R">R-R</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/V-PR" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/V-PR">V-PR</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-multi/V-ROC" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-multi">
            <label for="Metrics-multi/V-ROC">V-ROC</label>
          </div>
        </div>
      </div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div id='all-multi'>
      <div class='checkbox-container'>
        <div class="all-checkbox">
          <label for="select-all">
            <h3 style="white-space:nowrap">Datasets
              <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleSelectAll(true,'multi')" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleSelectAll(false,'multi')" style="padding:0 3px">off</a>]</b>
            </h3>
          </label>
        </div>
      </div>
      <div class="checkbox-container" id="dataset-container-multi"></div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div class="checkbox-container1" id="dataset-container-mul-down1">
      <div class="category" style="margin-bottom:0px">
        <h3>
          <input type="checkbox" id="select-all-Score-multi" style='display:none' onchange="toggleCategory('Score','multi', this.checked)">
          Score
        </h3>
        <div class="checkbox-wrapper3">
          <div class="checkbox-item">
            <input type="radio" id="Score-multi/1" value="Score/1" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-multi">
            <label for="Score/1">🥇</label>
          </div>
          <div class="checkbox-item">
            <input type="radio" id="Score-multi/2" value="Score/2" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-multi">
            <label for="Score/2">🥇 + 🥈 + 🥉</label>
          </div>
          <div class="checkbox-item" style="flex-wrap:nowrap;">
            <input type="radio" id="Score-multi/3" value="Score/3" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-multi">
            <label for="Score/3">
            <input type="number" id="score-multi/3/1" name="score/3/1" value="3" oninput="validateInput(this)"> × 🥇 + 
            <input type="number" id="score-multi/3/2" name="score/3/2" value="2" oninput="validateInput(this)"> × 🥈 + 
            <input type="number" id="score-multi/3/3" name="score/3/3" value="1" oninput="validateInput(this)"> × 🥉</label>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div style="width:100%;margin-top: 0;" class="table-container" id='table-container-mul'>
    <table id="multi" class="my-table2">
      <thead>
        <tr>
          <th>Rank</th>
          <th>Model</th>
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
<div style="height:10px"></div>

### Rules:

- For each anomaly detection algorithm, we count the number of times that the algorithm receives the gold, silver, and bronze medals, i.e., having the lowest, 2nd lowest, and 3rd lowest errors, shown as 🥇, 🥈, and 🥉, respectively.

- We provide three different types of scores for ranking the anomaly detection algorithms. First, the scores equal to the numbers of gold medals. Second, the scores are the sum of the numbers of gold, silver, and bronze medals. Third, the scores are the weighted sum of the gold, silver, and bronze medals, where the weights can be customized. The larger the score, the higher the ranking.

<script src="https://cdnjs.cloudflare.com/ajax/libs/PapaParse/5.3.0/papaparse.min.js"></script>
<script src='./modelMetricsDashboard.js'></script>
<script>
  loadDataAndInitializeSettings('uni')
  loadDataAndInitializeSettings('multi')
</script>

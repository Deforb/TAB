# Leaderboards

<script src="https://cdnjs.cloudflare.com/ajax/libs/PapaParse/5.3.0/papaparse.min.js"></script>

## Leaderboard for few-shot setting

<div class="main-container" id="main-container-few">
  <div class="checkbox-wrapper">
    <div class="checkbox-container" id="dataset-container-mul-type-few">
      <div class="category" style="margin-bottom:0px;width: 241px;">
        <h3>
          <input type="checkbox" id="select-all-type-few" style='display:none' onchange="toggleCategory('Type','few', this.checked)">
          Model Type
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Type','few', true)" style="padding:0 3px">all</a>]</b>
        </h3>
        <div class="checkbox-wrapper1">
          <div class="checkbox-item">
            <input type="checkbox" id="Type-few/Pretrain-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-few">
            <label >TS Pretrain Model</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Type-few/LLM-Based-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-few">
            <label >LLM Based Model</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Type-few/Specific-Model" onchange="handleChildCheckboxChange(event)" class="checkbox-Type-few">
            <label >Specific Model</label>
          </div>
        </div>
      </div>
    </div>
     <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div class="checkbox-container" id="dataset-container-mul-up-few">
      <div class="category" style="margin-bottom:0px">
        <h3>
          <input type="checkbox" id="select-all-Metrics-few" style='display:none' onchange="toggleCategory('Metrics','few', this.checked)">
          Metrics
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Metrics','few', true)" style="padding:0 3px">all</a>]</b>
        </h3>
        <div class="checkbox-wrapper1">
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-few/MAE" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-few">
            <label>MAE</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Metrics-few/MSE" onchange="handleChildCheckboxChange(event)" class="checkbox-Metrics-few">
            <label>MSE</label>
          </div>
        </div>
      </div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div id='all-few'>
      <div class='checkbox-container'>
        <div class="all-checkbox">
          <input type="checkbox" id="select-all" onclick="toggleSelectAll(this.checked,'few')" style="display:none">
          <label for="select-all">
            <h3 style="white-space:nowrap">Datasets
              <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleSelectAll(true,'few')" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleSelectAll(false,'few')" style="padding:0 3px">off</a>]</b>
            </h3>
          </label>
        </div>
      </div>
      <div class="checkbox-container" id="dataset-container-few"></div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div class="checkbox-container1" id="dataset-container-mul-down">
      <div class="category" style="margin-bottom:0px">
        <h3>
          <input type="checkbox" id="select-all-Horizons-few" style='display:none' onchange="toggleCategory('Horizons', this.checked)">
          Forecasting Horizons
          <b style="font: 16px 'Microsoft YaHei', Verdana, sans-serif; font-weight:bold"> [<a href="javascript:void(0);" onclick="toggleCategory('Horizons','few', true)" style="padding:0 3px">all</a>|<a href="javascript:void(0);" onclick="toggleCategory('Horizons','few', false)" style="padding:0 3px">off</a>]</b>
        </h3>
        <div class="checkbox-wrapper2">
          <div class="checkbox-item">
            <input type="checkbox" id="Horizons-few/96" onchange="handleChildCheckboxChange(event)" class="checkbox-Horizons-few">
            <label for="Horizons/96">96</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Horizons-few/192" onchange="handleChildCheckboxChange(event)" class="checkbox-Horizons-few">
            <label for="Horizons/192">192</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Horizons-few/336" onchange="handleChildCheckboxChange(event)" class="checkbox-Horizons-few">
            <label for="Horizons/336">336</label>
          </div>
          <div class="checkbox-item">
            <input type="checkbox" id="Horizons-few/720" onchange="handleChildCheckboxChange(event)" class="checkbox-Horizons-few">
            <label for="Horizons/720">720</label>
          </div>
        </div>
      </div>
    </div>
    <div style='width:95%'>
      <hr style="border:1px dashed #ddd">
    </div>
    <div class="checkbox-container1" id="dataset-container-mul-down1">
      <div class="category" style="margin-bottom:0px">
        <h3>
          <input type="checkbox" id="select-all-Score-few" style='display:none' onchange="toggleCategory('Score','few', this.checked)">
          Score
        </h3>
        <div class="checkbox-wrapper3">
          <div class="checkbox-item">
            <input type="radio" id="Score-few/1" value="Score/1" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-few">
            <label for="Score/1">🥇</label>
          </div>
          <div class="checkbox-item">
            <input type="radio" id="Score-few/2" value="Score/2" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-few">
            <label for="Score/2">🥇 + 🥈 + 🥉</label>
          </div>
          <div class="checkbox-item" style="flex-wrap:nowrap;">
            <input type="radio" id="Score-few/3" value="Score/3" onchange="handleChildCheckboxChange(event)" class="checkbox-Score-few">
            <label for="Score/3">
            <input type="number" id="score-few/3/1" name="score/3/1" value="3" oninput="validateInput(this)"> × 🥇 + 
            <input type="number" id="score-few/3/2" name="score/3/2" value="2" oninput="validateInput(this)"> × 🥈 + 
            <input type="number" id="score-few/3/3" name="score/3/3" value="1" oninput="validateInput(this)"> × 🥉</label>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div style="width:100%;margin-top: 0;" class="table-container" id='table-container-mul'>
    <table id="few" class="my-table2">
      <thead>
        <tr>
          <th>Rank</th>
          <th>Model</th>
          <th>Parameters</th>
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

- For short-term time series datasets like ILI, the sample size under the 5% sampling condition is insufficient to support fine-tuning of the foundation model. Therefore, we only conduct tests on long-term time series datasets.

- For time series foundation models, we consider 10 datasets and 2 error metrics, i.e., MAE and MSE. For each dataset, we consider 4 forecasting horizons. We default to uniformly sampling 5% of the samples from the training set for model fine-tuning and evaluation on test set.

- For each forecasting algorithm, we count the number of times that the algorithm receives the gold, silver, and bronze medals, i.e., having the lowest, 2nd lowest, and 3rd lowest errors, shown as 🥇, 🥈, and 🥉, respectively.

- We provide three different types of scores for ranking the forecasting algorithms. First, the scores equal to the numbers of gold medals. Second, the scores are the sum of the numbers of gold, silver, and bronze medals. Third, the scores are the weighted sum of the gold, silver, and bronze medals, where the weights can be customized. The larger the score, the higher the ranking.

<style>
/* 基本表格样式 */
table.my-table2 {
  width: 100%;
  border-collapse: collapse;
  font-family: Arial, sans-serif;
  border: none; /* 去除表格边框 */
  padding:0;
  margin:0
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
  margin:auto;
  overflow-y: hidden; /* Enable vertical scroll */
  display: flex;justify-content: LEFT;
}
 select {
    background-color: #f2f2f2; /* 表头背景色（奇数行浅灰色） */
    color: black; /* 表头文字颜色 */
    font-weight: bold; /* 表头字体加粗 */
    text-align: center; /* 居中对齐 */
    white-space: nowrap; /* 防止文本换行 */
    border: none;
    margin:auto;
    }
select:focus {
  border: none; /* 确保选中时没有边框 */
  outline: none; /* 确保选中时没有黑框 */
}
option
{
    padding:5px,0;
}
.checkbox-item
{
    margin-left:10px;
}
</style>

<style>
.main-container{
    display: flex;
    align-items: stretch; /* Stretch items to the same height */
    height: 100%;
}
.checkbox-container1
{
    display: grid;
    grid-template-columns: 1fr; /* 分为两列 */
    gap: 10px;
    padding-right: 20px; /* Add some space between checkboxes and table */
    overflow-y: auto; /* Enable vertical scroll if needed */
}
.checkbox-container {
 display: grid;
    grid-template-columns: 0.7fr 0.7fr; /* 分为两列 */
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
    width:fit-content;
}
.article-entry h3{
    margin:0;
    margin-right: 6px;
}
.all-checkbox {
    display: flex;
    align-items: center;
    margin-bottom: 10px; /* 在 "All" 复选框和其他复选框之间添加一些间距 */
}
.checkbox-wrapper1 {
    display: grid;
    grid-template-columns: 1fr;
    width:250px;

}

.checkbox-wrapper2 {
    display: grid;
    grid-template-columns: 1.5fr 1.5fr 1.5fr 1.5fr;
    width:260px;

}
.checkbox-wrapper3 {
    display: grid;
    grid-template-columns: 1;
    width:100%;

}
.checkbox-wrapper3 .checkbox-item
{
     margin-left:15px;
     margin-top:10px;
}
input[type="number"] {
    border: none; /* 去掉边框 */
    border-bottom: 1px solid #000; /* 底部添加一条横线 */
    outline: none;
    padding: 0px;
    /* padding-right: 0px;  */
    
    width: 31px;
    font-size:14px;
    /* text-align:right; */
    text-align:center;
}
input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
    -webkit-appearance: none;
}
input[type="number"]{
    -moz-appearance: textfield;
}

</style>

<style>
.sticky-col{
            background-color: white;
            position: sticky;
            left: 0; /* 固定在左侧 */
            z-index: 1;/* 设定堆叠顺序 */
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

<script>
  const MODEL_TYPE = {
  'Pretrain-Model': ['TimesFM', 'Timer', 'UniTS', 'TTM', 'MOIRAI', 'ROSE', 'Moment'],
  'LLM-Based-Model': ['GPT4TS', 'UniTime', 'S2IPLLM', 'TimeLLM'],
  'Specific-Model': [
    'PatchTST',
    'Dlinear',
    'FITS',
    'iTransformer',
    'FedFormer',
    'TimesNet',
    'TimeMixer',
  ],
}

const all_data = {
  zero: { method: {}, dataset: [], metric: [], result: {} },
  few: { method: {}, dataset: [], metric: [], result: {} },
  full: { method: {}, dataset: [], metric: [], result: {} },
}

// const settings = ['few', 'full']
const settings = ['few']

settings.forEach(setting => {
  fetch(`./${setting}.csv`)
    .then(response => response.text())
    .then(text =>
      Papa.parse(text, {
        header: true,
        dynamicTyping: true,
        complete: results => {
          for (let i1 = 1; i1 < 4; i1++) {
            const scoreBox = document.getElementById(`Score-${setting}/${i1}`)
            if (scoreBox != null) {
              scoreBox.checked = false
            } else {
              console.log(`no scoreBox of ${setting}/${i1}`)
            }
          }
          button = document.getElementById(`Score-${setting}/1`)
          if (button) button.checked = true
          phraseInputTable(results.data, setting)
          toggleCategory('Metrics', setting, true, false)
          toggleCategory('Type', setting, true, false)
          toggleCategory('Horizons', setting, true, false)
          // 设置评分选项
          toggleSelectAll(true, setting)
          // no use???
          // display(setting)
        },
      })
    )
})

function phraseInputTable(input, setting) {
  // phrase method
  const [
    contactTexts,
    contactUrls,
    paperUrls,
    codeUrls,
    publications,
    bibs,
    years,
    parametersList, // input[8] 未使用
    ,
    methods,
  ] = input

  const keys = Object.keys(methods).filter(item => item !== 'Dataset-Quantity-metrics')
  // 存入all_data
  keys.forEach(name => {
    all_data[setting].method[name] = {
      contact_text: contactTexts[name] || '',
      contact_url: contactUrls[name],
      paper_url: paperUrls[name],
      code_url: codeUrls[name],
      publication: publications[name],
      bib: bibs[name],
      year: years[name],
      parameters: parametersList[name],
    }
  })

  // Phrase result
  for (let i = 8; i < input.length; i++) {
    const entry = input[i]
    const key = entry['Dataset-Quantity-metrics']
    if (!key) continue

    const [data, horizon, metric] = key.split('-')

    if (!all_data[setting]['dataset'].includes(data)) {
      all_data[setting]['dataset'].push(data)
    }
    if (!all_data[setting]['metric'].includes(metric)) {
      all_data[setting]['metric'].push(metric)
    }
    all_data[setting].result[key] = entry
  }

  // 按大类分组数据集
  const groupedDatasets = all_data[setting].dataset.reduce((acc, dataset) => {
    const [category, name] = dataset.split('/')
    if (!acc[category]) acc[category] = []
    acc[category].push(name)
    return acc
  }, {})

  // 按数据集数量排序
  const sortedCategories =
    setting !== 'zero'
      ? Object.keys(groupedDatasets).sort(
          (a, b) => groupedDatasets[b].length - groupedDatasets[a].length
        )
      : [
          'Traffic',
          'Energy',
          'Environment',
          'Economic',
          'Nature',
          'Health',
          'Stock',
          'Banking',
          'Web',
          'Electricity',
        ]

  // 数据集选择区域
  const container = document.getElementById(`dataset-container-${setting}`)
  sortedCategories.forEach(category => {
    // 大标题
    const categoryDiv = document.createElement('div')
    categoryDiv.className = 'category'

    const categoryLabel = document.createElement('h3')
    const categoryCheckbox = document.createElement('input')
    categoryCheckbox.type = 'checkbox'
    categoryCheckbox.id = `select-all-${category}-${setting}`
    categoryCheckbox.addEventListener('change', () =>
      toggleCategory(category, setting, categoryCheckbox.checked)
    )

    categoryLabel.appendChild(categoryCheckbox)
    categoryLabel.appendChild(document.createTextNode(` ${category}`))
    categoryDiv.appendChild(categoryLabel)

    const datasetContainer = document.createElement('div')

    // 添加小标题
    groupedDatasets[category].forEach(name => {
      name = name.replace('_', '-')
      const checkboxItem = document.createElement('div')
      checkboxItem.className = 'checkbox-item'

      // ??? hardcode
      if (category === 'Electricity' && setting === 'zero') {
        checkboxItem.style = 'display:flex'
        datasetContainer.style = 'display:flex'
      }

      // 多选框
      const checkbox = document.createElement('input')
      checkbox.type = 'checkbox'
      checkbox.id = `${category}-${setting}/${name}`
      checkbox.value = `${category}-${setting}/${name}`
      checkbox.className = `checkbox-${category}-${setting}`
      checkbox.addEventListener('change', handleChildCheckboxChange)

      // 标签
      const label = document.createElement('label')
      label.htmlFor = `${category}/${name}`
      label.textContent = name

      checkboxItem.appendChild(checkbox)
      checkboxItem.appendChild(label)
      datasetContainer.appendChild(checkboxItem)
    })

    categoryDiv.appendChild(datasetContainer)
    container.appendChild(categoryDiv)
  })
}

// 子复选框改变事件
function handleChildCheckboxChange(event) {
  const checkbox = event.target
  const [_, category, setting] = checkbox.className.split('-')

  // score 是单选框
  if (category === 'Score') {
    checkbox.checked = true
    const checkboxId = checkbox.value
    // 获取所有相关的Score复选框并取消选中非当前选中的
    for (let i = 1; i < 4; i++) {
      const scoreBox = document.getElementById(`Score-${setting}/${i}`)
      if (scoreBox && scoreBox.value !== checkboxId) {
        scoreBox.checked = false
      }
    }
  } else {
    // 处理多选框的父级逻辑
    updateParentCheckbox(category, setting)
  }
  submitSelection(setting)
}

/**
 * Toggles the checked state of checkboxes for a specific category and setting.
 *
 * @param {string} category - The category identifier.
 * @param {string} setting - The setting identifier.
 * @param {boolean} isChecked - Determines whether the checkboxes should be checked or unchecked.
 * @param {boolean} [flush=true] - Whether to submit the selection after toggling.
 */
function toggleCategory(category, setting, isChecked, flush = true) {
  const checkboxes = document.querySelectorAll(`.checkbox-${category}-${setting}`)
  checkboxes.forEach(checkbox => {
    checkbox.checked = isChecked
  })
  if (flush) submitSelection(setting)
}

/**
 * Toggles the selection state of all checkboxes based on the selectAllCheckbox value.
 *
 * @param {boolean} selectAllCheckbox - Determines whether to select or deselect all checkboxes.
 * @param {string} setting - The specific setting identifier used to locate the relevant checkbox container.
 */
function toggleSelectAll(selectAllCheckbox, setting) {
  const container = document.getElementById(`all-${setting}`)
  const checkboxes = container.querySelectorAll('input[type="checkbox"]')
  checkboxes.forEach(checkbox => {
    checkbox.checked = selectAllCheckbox
  })
  submitSelection(setting)
}

// function display(setting) {
//   table = `display-${setting}`
//   const tableHeadr = document.getElementById(table).getElementsByTagName('thead')[0]
//   const tableBody = document.getElementById(table).getElementsByTagName('tbody')[0]
//   const rowHeadr1 = document.createElement('tr')
//   const rowHeadr2 = document.createElement('tr')
//   const rowHeadr3 = document.createElement('tr')

//   result = Object.values(all_data[setting]['result'])
//   result.sort((a, b) => {
//     if (a['Dataset-Quantity-metrics'].split('-')[0] != b['Dataset-Quantity-metrics'].split('-')[0])
//       return a < b

//     if (a['Dataset-Quantity-metrics'].split('-')[1] == b['Dataset-Quantity-metrics'].split('-')[1])
//       return a < b

//     return (
//       Number(a['Dataset-Quantity-metrics'].split('-')[1]) >
//       Number(b['Dataset-Quantity-metrics'].split('-')[1])
//     )
//   })

//draw table head
// method = Object.keys(result[0])
// td1 = document.createElement('td')
// td1.innerHTML = 'Model'
// td1.rowSpan = 2
// td1.colSpan = 2
// td1.style = 'font-weight:bold;left:0;background-color:#f2f2f2;top:0;z-index:3;'
// td1.className = 'sticky-col-header sticky-col2'
// rowHeadr1.appendChild(td1)
// td2 = document.createElement('td')
// td2.innerHTML = 'Metrics'
// td2.colSpan = 2
// td2.style = 'font-weight:bold;left:0;background-color:#f2f2f2;top:63.4px;z-index:3;'
// td2.className = 'sticky-col-header sticky-col2'
// rowHeadr3.appendChild(td2)
// method = method.filter(
//   a => a != 'Dataset-Quantity-metrics' && Object.keys(all_data[setting]['method']).includes(a)
// )
// method.sort((b, a) => all_data[setting]['method'][a].year - all_data[setting]['method'][b].year)
// method.forEach(key => {
//   td1 = document.createElement('td')
//   td1.innerHTML = key
//   td1.colSpan = 2
//   td1.style = 'font-weight:bold'
//   rowHeadr1.appendChild(td1)

//   td2 = document.createElement('td')
//   td2.innerHTML = all_data[setting]['method'][key].year
//   td2.style = 'padding:0;font-weight:bold;'
//   td2.colSpan = 2
//   rowHeadr2.appendChild(td2)

//   td3 = document.createElement('td')
//   td3.innerHTML = 'MSE'
//   td3.style = 'font-weight:bold'
//   td4 = document.createElement('td')
//   td4.innerHTML = 'MAE'
//   td4.style = 'font-weight:bold'
//   rowHeadr3.appendChild(td3)
//   rowHeadr3.appendChild(td4)
// })

// rowHeadr1.style = 'background-color:#f2f2f2;font-weight:bold;top:0;z-index: 3;'
// rowHeadr1.className = 'sticky-th'
// rowHeadr2.style =
//   'background-color:#f2f2f2;padding: 0px;height: 25px;font-size: 14px;font-weight:bold;top:38.4px;'
// rowHeadr2.className = 'sticky-th'
// rowHeadr3.style =
//   'background-color:#f2f2f2;font-weight:bold;top:63.4px;box-shadow: rgba(0, 0, 0, 0.4) 0px 2px 3px -2px;'
// rowHeadr3.className = 'sticky-th'
// tableHeadr.appendChild(rowHeadr1)
// tableHeadr.appendChild(rowHeadr2)
// tableHeadr.appendChild(rowHeadr3)

// // draw table body
// for (let i = 0; i < result.length; i = i + 8) {
//   const row1 = document.createElement('tr')
//   const row2 = document.createElement('tr')
//   const row3 = document.createElement('tr')
//   const row4 = document.createElement('tr')

//   td = document.createElement('td')
//   td.innerHTML = result[i]['Dataset-Quantity-metrics'].split('-')[0].split('/')[1]
//   td.className = 'sticky-col-header sticky-col2'
//   td.rowSpan = 4

//   if ((i / 8) % 2 == 0) {
//     td.style =
//       ' writing-mode: vertical-rl; transform: rotate(180deg);margin:auto;text-rendering: geometricPrecision; -webkit-font-smoothing: antialiased;-moz-osx-font-smoothing: grayscale; width: 20px;background-color:#fff;left:0; '
//   } else {
//     td.style =
//       ' writing-mode: vertical-rl; transform: rotate(180deg);margin:auto;text-rendering: geometricPrecision; -webkit-font-smoothing: antialiased;-moz-osx-font-smoothing: grayscale; width: 20px;background-color:#f2f2f2;left:0; '
//   }
//   row1.appendChild(td)
//   rowList = [row1, row2, row3, row4]
//   horenzon = ['96', '192', '336', '720']
//   for (let j = 0; j < rowList.length; j = j + 1) {
//     td_horenzon = document.createElement('td')
//     td_horenzon.innerHTML = horenzon[j]
//     if (j % 2 == 1) {
//       td_horenzon.style = 'background-color:#f2f2f2;left:29.35px;'
//     } else {
//       td_horenzon.style = 'background-color:#fff;left:29.35px ;'
//     }
//     td_horenzon.className = 'sticky-col-header sticky-col2'
//     rowList[j].appendChild(td_horenzon)
//     rowData1 = result[i + 2 * j]
//     method.sort((a, b) => {
//       if (rowData1[a] == '-') return 1
//       if (rowData1[b] == '-') return -1
//       return rowData1[a] - rowData1[b]
//     })
//     sort1 = structuredClone(method)
//     rowData2 = result[i + 2 * j + 1]
//     method.sort((a, b) => {
//       if (rowData2[a] == '-') return 1
//       if (rowData2[b] == '-') return -1
//       return rowData2[a] - rowData2[b]
//     })
//     sort2 = structuredClone(method)
//     Object.keys(rowData1).forEach(key => {
//       if (key != 'Dataset-Quantity-metrics') {
//         td1 = document.createElement('td')
//         td1.innerHTML = processData(rowData1, key, sort1)
//         rowList[j].appendChild(td1)
//         td2 = document.createElement('td')
//         td2.innerHTML = processData(rowData2, key, sort2)
//         rowList[j].appendChild(td2)
//       }
//     })
//     tableBody.appendChild(rowList[j])
//   }
// }
// }

// function processData(rowData, key, sort) {
//   input = rowData[key]
//   if (input == '-') return input
//   if (key == sort[0]) {
//     return `<b> ${parseFloat(input).toFixed(3)} </b>`
//   } else if (key == sort[1]) {
//     return `<p class="double-underline"> ${parseFloat(input).toFixed(3)}</p>`
//   } else if (key == sort[2]) {
//     return `<u> ${parseFloat(input).toFixed(3)} </u>`
//   } else {
//     return `${parseFloat(input).toFixed(3)}`
//   }
// }

/**
 * Updates the state of the parent checkbox based on the state of child checkboxes.
 *
 * @param {string} category - The category identifier used to select the related checkboxes.
 * @param {string} setting - The setting identifier used to select the related checkboxes.
 */
function updateParentCheckbox(category, setting) {
  if (category.includes('Type')) return

  const checkboxes = document.querySelectorAll(`.checkbox-${category}-${setting}`)
  const selectAllCheckbox = document.getElementById(`select-all-${category}-${setting}`)

  for (const checkbox of checkboxes) {
    if (!checkbox.checked) {
      selectAllCheckbox.checked = false
      return
    }
  }

  selectAllCheckbox.checked = true
}

function submitSelection(setting) {
  // 获取所有的 checkbox
  const checkboxes = document.querySelectorAll(`*[class*="${setting}"]`)
  const selectTypes = []
  const selectMetrics = []
  const selectHorizons = []
  const selectDatasets = []
  let selectScore = null

  // Iterate through each checkbox and categorize based on its ID
  checkboxes.forEach(checkbox => {
    if (checkbox.checked) {
      const idParts = checkbox.id.split('/')
      if (checkbox.id.includes('Type')) {
        selectTypes.push(idParts[1].trim())
      } else if (checkbox.id.includes('Metrics')) {
        selectMetrics.push(idParts[1])
      } else if (checkbox.id.includes('Score')) {
        selectScore = idParts[1].split('-')[0]
      } else if (checkbox.id.includes('Horizons')) {
        selectHorizons.push(idParts[1])
      } else {
        const dataset = `${checkbox.id.split('-')[0]}/${idParts[1]}`
        selectDatasets.push(dataset)
      }
    }
  })

  // Banking/NN5-192-mae
  const rank = {}
  let selectedMethods = []

  if (setting === 'zero') {
    // Predefined methods for 'zero' setting
    ;['TimesFM', 'Timer', 'UniTS', 'TTM', 'MOIRAI', 'ROSE'].forEach(method => {
      rank[method] = { rank1: 0, rank2: 0, rank3: 0, score: 0 }
    })
  } else {
    // If no types are selected, include all types and reset datasets
    if (selectTypes.length === 0) {
      selectTypes.push('Pretrain-Model', 'LLM-Based-Model', 'Specific-Model')
      selectDatasets.length = 0
    }
    // Aggregate methods based on selected types
    selectTypes.forEach(type => {
      selectedMethods = selectedMethods.concat(MODEL_TYPE[type])
    })
    // Filter methods that exist in all_data
    console.log(all_data[setting])

    selectedMethods = selectedMethods.filter(selectedMethod =>
      all_data[setting].method.hasOwnProperty(selectedMethod)
    )
  }

  // Initialize rank object for each selected method
  selectedMethods.forEach(method => {
    rank[method] = { rank1: 0, rank2: 0, rank3: 0, score: 0 }
  })

  // Process selected metrics, horizons, and datasets to update rankings
  selectMetrics.forEach(metric => {
    selectHorizons.forEach(horizon => {
      selectDatasets.forEach(dataset => {
        const key = `${dataset}-${horizon}-${metric.toLowerCase()}`
        const result = all_data[setting].result[key]
        sortedKeys = selectedMethods.sort((a, b) => result[a] - result[b])
        rank[sortedKeys[0]].rank1 += 1
        rank[sortedKeys[1]].rank2 += 1
        rank[sortedKeys[2]].rank3 += 1
      })
    })
  })

  const rowDatas = []
  // 根据记分方式计算总分
  Object.keys(rank).forEach(method => {
    if (selectScore === '3') {
      const weight1 = document.getElementById(`score-${setting}/3/1`).value || 0
      const weight2 = document.getElementById(`score-${setting}/3/2`).value || 0
      const weight3 = document.getElementById(`score-${setting}/3/3`).value || 0
      rank[method].score =
        rank[method].rank1 * weight1 + rank[method].rank2 * weight2 + rank[method].rank3 * weight3
    } else if (selectScore === '2') {
      rank[method].score = rank[method].rank1 + rank[method].rank2 + rank[method].rank3
    } else {
      rank[method].score = rank[method].rank1
    }
    rowDatas.push({
      method,
      score: rank[method].score,
      // score: rank[method].score.toFixed(2),
      rank1: rank[method].rank1,
      rank2: rank[method].rank2,
      rank3: rank[method].rank3,
    })
  })

  // Sort the draw array based on score and ranks
  rowDatas.sort((a, b) => {
    if (b.score !== a.score) return b.score - a.score
    if (b.rank1 !== a.rank1) return b.rank1 - a.rank1
    if (b.rank2 !== a.rank2) return b.rank2 - a.rank2
    return b.rank3 - a.rank3
  })

  // Render the table with the calculated draw data
  draw_table(rowDatas, setting)
}

function draw_table(rowDatas, setting) {
  const tbody = document.querySelector(`#${setting} tbody`)
  tbody.innerHTML = ''
  const fragment = document.createDocumentFragment()

  function formatNumber(num) {
    // if (num >= 1e9) {
    //     return (num / 1e9).toFixed(1) + 'B';  // 表示十亿
    // } else if (num >= 1e6) {
    //     return (num / 1e6).toFixed(1) + 'M';  // 表示百万
    // } else if (num >= 1e3) {
    //     return (num / 1e3).toFixed(1) + 'K';  // 表示千
    // } else {
    //     return num.toString();  // 小于千的数字
    // }
    return (num / 1e6).toFixed(2) + 'M'
  }

  rowDatas.forEach((rowData, index) => {
    const { method, score, rank1, rank2, rank3 } = rowData
    const methodData = all_data[setting].method[method]
    const { parameters, paper_url, publication, bib, year } = methodData

    const row = document.createElement('tr')
    row.innerHTML = `
      <td>${index + 1}</td>
      <td>${method}</td>
      <td>${formatNumber(parameters)}</td>
      <td>${score}</td>
      <td>${rank1}</td>
      <td>${rank2}</td>
      <td>${rank3}</td>
      <td><a href="${paper_url}" target="_blank">paper</a></td>
      <td>${publication} [<a href="${bib}" target="_blank">bib</a>]</td>
      <td>${year}</td>
    `
    fragment.appendChild(row)
  })

  tbody.appendChild(fragment)
}

let lastValidValue = ''
function validateInput(input, setting = 'few') {
  let value = input.value

  // 保存光标位置
  const cursorPos = input.selectionStart

  // 处理整数和小数部分
  let [integerPart, decimalPart] = value.split('.')

  // 处理整数部分：去除前导零并限制最大两位数

  // 去除前导零
  if (integerPart.length > 1) {
    integerPart = integerPart.replace(/^0+/, '')
  }

  // 处理小数部分：限制最多两位
  if (decimalPart) {
    decimalPart = decimalPart.slice(0, 2)
  }

  // 合并整数部分和小数部分
  let newValue = integerPart
  if (decimalPart) {
    newValue += `.${decimalPart}`
  }

  // 如果小数点后有数字，但是小数点前的数字部分为空，应至少显示 `0`
  if (newValue === '' || newValue === '.') {
    newValue = '0'
  }

  // 验证并更新输入值
  if (newValue !== value) {
    input.value = newValue
  }

  // 更新最后一个有效值
  lastValidValue = input.value

  // 恢复光标的位置
  // input.setSelectionRange(cursorPos, cursorPos);
  submitSelection(setting)
}

</script>

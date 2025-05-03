# TAB Overview

TAB is an open-source library designed for time series anomaly detection researchers.

<div style="height:5px"></div>

---

<div class="main-wrapper">
  <div class="content-block">
    <div class="block-section picture">
      <img src="figures/timeseries.svg" />
    </div>
    <div class="block-section heading">
      <a href="datasets/"><h2>Comprehensive Datasets</h2></a>
    </div>
    <div class="block-section description">
      <p lang="en">
        TAB encompasses 18 public multivariate time series datasets and 1,671 univariate time series from different domains to facilitate more comprehensive evaluations on diverse datasets.
      </p>
    </div>
  </div>
  <div class="content-block">
    <div class="block-section picture">
      <img src="figures/alg_icon.svg" />
    </div>
    <div class="block-section heading">
      <a href="algorithms/methods"><h2>Rich Algorithms</h2></a>
    </div>
    <div class="block-section description">
      <p>
        TAB covers a variety of TSAD methods, including Non-learning, Machine learning, Deep learning, LLM-based, and Time-series pre-trained methods.
      </p>
    </div>
  </div>
  <div class="content-block">
    <div class="block-section picture">
      <img src="figures/pipeline.svg" />
    </div>
    <div class="block-section heading">
      <a href="get started/#Pipeline-introduction"><h2>Unified Pipeline</h2></a>
    </div>
    <div class="block-section description">
      <p>
        TAB features a unified and automated evaluation pipeline that enables fair and easy evaluation of TSAD methods.
      </p>
    </div>
  </div>
</div>

<style>
.main-wrapper {
    display:flex;
    justify-content:space-between;
    width:100%;
    margin-top:3%;
    gap:20px;
}

.content-block {
    display:flex;
    flex-direction:column;
    width:33%;
    box-sizing:border-box;
}

.block-section {
    margin-bottom:5%;
    text-align:center; /* Ensure elements within are centered */
}

.picture img {
    width:auto;
    height:80px;
    display:block;
    margin:0 auto; /* Center the image */
    padding:0;
    padding-bottom:5%;
}

.heading h2 {
    color:#1195db;
    font-weight:bold;
    text-align:center;
    margin-top:-10%;
    padding:0;
}
.description{
    display:flex;
    justify-content:center;
    width:100%
}
.description p {
    text-align:left;
    margin-top:-10%;
    padding:0px 0;
    width:100%;
    font-size:14px;
}

a {
    color:#1195db; /* Link color */
}

</style>
<style>
.container {
    display: flex;
    /* width: 80%; */
    max-width: 1200px;
    /* box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); */
    background-color: #fff;
}
.left-column {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    /* padding: 20px; */
    /* margin-left:-135px; */
    /* border-right: 1px solid #ddd; */
}

.left-column .image {
    /* width: 100%; */
    height: 215px;
    width: 450px; 控制图片最大宽度
    /* height:215px; */
}

.left-column .left-text {
    margin-top: -10px;
    text-align: center;
}

.right-column {
    display: flex;
    flex-direction: column;
    padding: 20px;
    padding-left:0px;
    padding-top:0px;
    width:450px;
}

.right-column .top-text, .right-column .bottom-text {
    flex: 1;
    margin-bottom: 20px;
    height:170px;
}
.top-text
{
    width:500px;
}
.right-column .bottom-text {
    margin-bottom: 0;
}
.right-column .bottom-text .a {
   color:#1195db;
}

.right-column p {
    margin: 0;
}
        .text-content {
            width:30%;
            padding:0;
            /* margin-right:2%; */
        }
        .text-content h1 {
            font-size:1.5em;
            margin-top:0;
            margin-bottom:0;
        }
        .text-content p {
            font-size:1em;
            margin:0;
        }
        .image-content {
            text-align:center;
            padding:0;
            width:40%;
        }
        .image-content img {
            max-width:100%;
            height:auto;
            box-shadow:0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .download {
            width:30%;
            padding:0;
            display:flex;
            align-items:center;
            text-align:center;
        }
        .download img {
            width:80%;
            height:auto;
        }
        .download a {
            text-decoration:none;
            color:#0073e6;
            margin-top:0.5em;
            font-size:1.5em;
        }
.uuu {
    text-decoration:none;
    color:#1195db;
    margin-top:0.5em;
    font-size:1.5em;
}
 .copy-container {
            max-width: 600px;
            margin: 50px auto;
            text-align: center;
        }
        textarea {
            width: 100%;
            height: 200px;
        }
        button {
            margin-top: 10px;
            padding: 10px 20px;
            font-size: 16px;
        }
        .article-entry .highlight .line 
        {
            font-size:17px;
            line-height:0.8;
        }
        .article-entry .highlight .gutter pre 
        {
            display:none;
        }
</style>

<!-- ------

The below figure provides a visual overview of OpenTS's pipeline.

![](figures/Pipeline.png)

------

The table below provides a visual overview of how OpenTS's key features compare to other libraries for time series forecasting.

![](figures/Comparison_with_Related_Libraries.png)

 -->

---

<script>
function alter(){
    console.log('alter')
    // var total = 0
    // // while(total<4)
    // // {
    //   setTimeout(() => {
    //     var links = document.querySelectorAll('a');
    //     links.forEach(function(link) {
    //         // 如果 href 包含 'figures/paper.png'
    //         console.log(link.href)
    //         if (link.href.includes('svg')) {

    //         link.onclick = function(event) {
    //         event.preventDefault(); // 阻止默认的点击行为
    //         };
    //             link.style.pointerEvents = 'none';
    //         }
    //         else if (link.href.includes('paper.png')) {
    //             link.href = 'https://www.vldb.org/pvldb/vol17/p2363-hu.pdf';
                
    //         }
    //     })
    //     }, 5000);
    // }
    // var link =document.getElementBy
}
</script>

<!-- <h3 >Paper</h3>
<div class="container">
    <div class="left-column">
        <div class="left-text">
           <a href="https://www.vldb.org/pvldb/vol17/p2363-hu.pdf" > <h3 >PVLDB 2024 Best Research Paper Nomination</h3></a>
        </div>
            <a href="https://www.vldb.org/pvldb/vol17/p2363-hu.pdf" target="_blank" rel="noopener" >
            <img id="clickable-image" src="figures/paper.png" onload="alter()" class="image" style="box-shadow:0 2px 8px rgba(0, 0, 0, 0.1)">
            </a>
    </div>
    <div class="left-column">
        <div class="left-text">
            <a href="https://arxiv.org/pdf/2410.11802" > <h3 >arXiv</h3></a>
        </div>
                <a href="https://arxiv.org/pdf/2410.11802" target="_blank" rel="noopener" >
                <img id="clickable-image" src="figures/FoundTS.png" onload="alter()" class="image" style="box-shadow:0 2px 8px rgba(0, 0, 0, 0.1)">
                </a>
    </div>
</div> -->

<!-- <h3 >Cite us</h3>
<div class="container">
    <div class="right-column">
   ```bibtex
@article{qiu2024tfb,
  title   = {TFB: Towards Comprehensive and Fair Benchmarking of Time Series Forecasting Methods},
  author  = {Qiu, Xiangfei and Hu, Jilin and Zhou, Lekui and Wu, Xingjian and Du, Junyang and Zhang, Buang and Guo, Chenjuan and Zhou, Aoying and Jensen, Christian S and Sheng, Zhenli and Bin Yang},
  journal = {Proc. {VLDB} Endow.},
  year    = {2024},
  pages   = {2363 - 2377},
  volume  = {17}
}
```
    </div>
    <div class="right-column" style="margin-left:30px">
     ```bibtex
    @article{li2024foundts,
        title  = {FoundTS: Comprehensive and Unified Benchmarking of Foundation Models for Time Series Forecasting},
        author = {Zhe Li and Xiangfei Qiu and Peng Chen and Yihang Wang and Hanyin Cheng and Yang Shu and Jilin Hu and Chenjuan Guo and Aoying Zhou and Qingsong Wen and Christian S. Jensen and Bin Yang},
        year   = {2024},
        eprint = {2410.11802},
        archivePrefix = {arXiv}
    }
    ```
    </div>

</div> -->

<h3>Visitors</h3>

<script type='text/javascript' id='clustrmaps' src='//cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=278&t=n&d=ci3q8pHcV1YP18Iajpcs5SiRkYyBx90UXA0SkVpfzpU'></script>
<!-- <script type="text/javascript" id="clustrmaps" src="//clustrmaps.com/map_v2.js?d=ci3q8pHcV1YP18Iajpcs5SiRkYyBx90UXA0SkVpfzpU&cl=ffffff&w=a"></script> -->
<!-- <script type='text/javascript' id='clustrmaps' src='//cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=300&t=n&d=79WsHTeP81NNR9W0EkNAmSZhjG9nq02p5uyJImsO1i4'></script> -->
<!--
<h3 >About Us</h3>
        <div class="bottom-text">
            <a  href="https://decisionintelligence.github.io/index/"  style="color:#1195db;font-size:15px"> &nbsp;Decision Intelligence Lab</a>,
            <a  href="https://dase.ecnu.edu.cn/" style="color:#1195db;font-size:15px"> &nbsp;School of Data Science and Engineering</a>,
            <a  href="https://www.ecnu.edu.cn/"  style="color:#1195db;font-size:15px" >East China Normal University</a>
        </div> -->

  <!-- <div class="container">
        <div class="text-content">
            <h1>OpenTS paper</h1>
            <p>presents the datasets, benchmark experiments, and research opportunities.</p>
        </div>
        <div class="image-content">
            <img src="figures/paper.png">
        </div>
        <div class="download">
            <img src="figures/download.png">
            <a href="https://arxiv.org/abs/2403.20150">Download paper here</a>
        </div>
   </div> -->

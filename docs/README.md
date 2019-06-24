<script src="../pkgs/echarts.min.js"></script>
# <audio autoplay="" loop=""><source src="/_media/chengdu.mp3"></audio>
# ChengduExploration


  
<html><body><p><font size="4" color="gray">
The state comes into existence, originating in the bare needs of life, and continuing in existence for the sake of a good life. 

-- The Politics Of Aristotle, by Aristotle
</font></p></body></html>


## Change in Times
### Overview of Economy
Chengdu, located in the southwest of China, has been recently acknowledged as one of the fastest growing
cities in China. In recent years, its reputation has changed from "Heavenly Land of Plenty " with hot pots
and giant pandas to one of the most important engines of economy and technology in China.


While it is clear that the economy has dramatically changed over time, the answer to exactly how the economy has changed is a little more nuanced. One aim of this set of visualizations is to answer the question of how Chengdu's economic landscape has changed from 2009 to 2017.


The total economic output of Chengdu has a considerable proportion in Sichuan Province, and this uneven allocation of resources within the region will be further visualized.
```chart
{
	settings: {
    width: '100%',
    height: '300px'
  },
    title: {
        text: 'GDP Data'
    },
    tooltip : {
        trigger: 'axis',
        axisPointer: {
            type: 'cross',
            label: {
                backgroundColor: '#6a7985'
            }
        }
    },
    legend: {
        data:['Chengdu','Sichuan']
    },
    toolbox: {
        feature: {
            saveAsImage: {}
        }
    },
    grid: {
        left: '3%',
        right: '4%',
        bottom: '3%',
        containLabel: true
    },
    xAxis : [
        {
            type : 'category',
            boundaryGap : false,
            data : ['2009','2010','2011','2012','2013','2014','2015','2016','2017']
        }
    ],
    yAxis : [
        {
            type : 'value'
        }
    ],
    series : [
        {
            name:'Chengdu',
            type:'line',
            stack: '总量',
            areaStyle: {},
            data:[4503, 5551.3, 6854.58, 8138.9, 9108.89, 10056.59, 10801.16,12170.23,13889.39]
        },
        {
            name:'Sichuan',
            type:'line',
            stack: '总量',
            areaStyle: {},
            data:[14151.28, 17185.48, 21026.68, 23872.8, 26392.07, 28536.66, 30053.1,32934.54,36980.22]
        }
    ]
}

```

<br/>
```chart
{
"backgroundColor" : "#344b57",
"title": {
        "text": 'GDP Structure of Chengdu',
		x:"4%",
	textStyle:{
		color:"#fff",
		fontSize:'22'
    },
	subtextStyle:{
		color:'#90979c',
		fontSize:'16',
		
	},
},
	'tooltip':{
		"trigger":"axis",
		"axisPointer":{
			"type":"shadow",
			textStyle:{
				color:"#fff"
			}
		},
	},
	"grid":{
		"borderWidth":0,
		"top":110,
		"bottom":95,
		textStyle:{
			color:"#fff"
		}
	},
	"legend":{
		x: "4%",
		top: '11%',
		textStyle:{
			color: '#90979c',
		},
		"data":["Primary Industry","Secondary Industry","Tertiary Industry","Whole GDP"]
	},
	
	"calculable":true,
	
    xAxis: [{
		'type':'category',
		
        data: ['2009','2010','2011','2012','2013','2014','2015','2016','2017'],
        'splitLine':{
			'show': false
		},
        axisTick: {
            show: false
        },
		"splitArea":{
			"show":false
		},
        axisLine: {
			lineStyle: {
				color: '#90979c'
			}
        },
    }],
    yAxis: [{
		"type":"value",
                "max":15000,
		"splitLine":{
			"show":false
		},
        "axisLine": {
            lineStyle:{
				color:"#90979c"
			}
        },
        "axisTick": {
            "show": false
        },
        axisLabel: {
            "interval":0,
        },
		"splitArea":{
			"show":false
		},
		
    }],
     dataZoom: [
        {   // 这个dataZoom组件，默认控制x轴。
            type: 'slider', // 这个 dataZoom 组件是 slider 型 dataZoom 组件
            start: 10,      // 左边在 10% 的位置。
            end: 60         // 右边在 60% 的位置。
        },
        {   // 这个dataZoom组件，也控制x轴。
            type: 'inside', // 这个 dataZoom 组件是 inside 型 dataZoom 组件
            start: 10,      // 左边在 10% 的位置。
            end: 60         // 右边在 60% 的位置。
        }
    ],
    series: [
		{
		"name":"Primary Industry",
		'type':'bar',
		'stack':'总量',
		'barMaxWidth':35,
		'barGap':'10%',
		'itemStyle':{
			'normal':{
				'color':'rgba(144,280,128,1)',
				'label':{
					'show':true,
					'textStyle':{
						'color':"#fff"
					},
					'position':'insideBottom',
					formatter: function(p){
						return p.value > 0 ? (p.value):"";
					}
				}
			}
		},
		'data':[
		267.77,
		285.1,
		327.34,
		348.1,
		353.17,
		357.07,
		373.15,
		474.94,
		500.87
		]
		},
		
		{
		"name":"Secondary Industry",
		'type':'bar',
		'stack':'总量',
		'barMaxWidth':35,
		'barGap':'10%',
		'itemStyle':{
			'normal':{
				'color':'rgba(255,144,128,1)',
				'label':{
					'show':true,
					'textStyle':{
						'color':"#fff"
					},
					'position':'insideBottom',
					formatter: function(p){
						return p.value > 0 ? (p.value):"";
					}
				}
			}
		},
		'data':[2001.80,2480.90,3143.82,3143.820,3143.82,4508.53,4723.49,5232.02,5998.19]
		},
		
		{
		"name":"Tertiary Industry",
		'type':'bar',
		'stack':'总量',
		'barMaxWidth':35,
		'barGap':'10%',
		'itemStyle':{
			'normal':{
				'color':'rgba(0,191,183,1)',
				'label':{
					'show':true,
					'textStyle':{
						'color':"#fff"
					},
					'position':'insideBottom',
					formatter: function(p){
						return p.value > 0 ? (p.value):"";
					}
				}
			}
		},
		'data':[2233.04, 2785.30, 3383.42, 4025.2, 4574.23, 5190.99, 5704.52,6463.27,7390.34]
		},
		
		{
		"name":"Whole GDP",
		'type':'line',
		'stack':'总量2',
		symbolSize:10,
		symbol:'circle',
		'itemStyle':{
			'normal':{
				'color':'rgba(128,100,280,1)',
				'label':{
					'show':true,
					'textStyle':{
						'color':"#fff"
					},
					'position':'insideTop',
					formatter: function(p){
						return p.value > 0 ? (p.value):"";
					}
				}
			}
		},
		'data':[4503, 5551.3, 6854.58, 8138.9, 9108.89, 10056.59, 10801.16,12170.23,13889.39]
		},
		
		
	]
	}

```

### Dive into Economy data

<span style="font-size: 20px; font-weight: 600">Employment</span> is the most important economic indicator besides economic growth, and the employment population that the city can accommodate is an important symbol to determine the scale of its urban development.We select the employment population data of Sichuan Province in 2016 to analyze the employment population of each major city.
```chart
{
    backgroundColor: '#2c343c',

    title: {
        text: 'Employment Population of Sichuan in 2016',
        left: 'center',
        top: 20,
        textStyle: {
            color: '#ccc'
        }
    },

    tooltip : {
        trigger: 'item',
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },

    visualMap: {
        show: false,
        min: 80,
        max: 600,
        inRange: {
            colorLightness: [0, 1]
        }
    },
    series : [
        {
            name:'Cities',
            type:'pie',
            radius : '55%',
            center: ['50%', '50%'],
            data:[
                {value:879.02, name:'Chengdu'},
                {value:222.97, name:'Deyang'},
                {value:303.80, name:'Mianyang'},
                {value:253.15, name:'Luzhou'},
                {value:297.86, name:'Nanchong'},
				{value:332.00,name:"Dazhou"},
				{value:169.46,name:'Zigong'},
				{value:164.50,name:'Guangyuan'},
				{value:162.72,name:'Suining'},
				{value:176.57,name:'Neijiang'},
				{value:185.13,name:'Leshan'},
				{value:315.81,name:'Yibin'},
				{value:218.26,name:'Guangyuan'},
				{value:1178.75,name:'Others'}
            ].sort(function (a, b) { return a.value - b.value; }),
            roseType: 'radius',
            label: {
                normal: {
                    textStyle: {
                        color: 'rgba(255, 255, 255, 0.3)'
                    }
                }
            },
            labelLine: {
                normal: {
                    lineStyle: {
                        color: 'rgba(255, 255, 255, 0.3)'
                    },
                    smooth: 0.2,
                    length: 10,
                    length2: 20
                }
            },
            itemStyle: {
                normal: {
                    color: '#c23531',
                    shadowBlur: 200,
                    shadowColor: 'rgba(0, 0, 0, 0.5)'
                }
            },

            animationType: 'scale',
            animationEasing: 'elasticOut',
            animationDelay: function (idx) {
                return Math.random() * 200;
            }
        }
    ]
}
```


In addition to employment, the level of growth in personal income can reflect the rise in the living standards of residents in the region.


```chart
{
	color: ['#5793f3','#d14a61','#675bba'],
	
	tooltip:{
		trigger:'axis',
		axisPointer:{type:'cross'}
	},
	grid:{
		right:'20%'
	},
	toolbox:{
		feature:{
			dataView:{show:true,readOnly:false},
			restore:{show:true},
			saveAsImage:{show:true}
		}
	},
	legend:{
		data:['Average wage of Chengdu','Average wage of Sichuan','Per capita GDP of Chengdu']
	},
	xAxis:[
		{
			type:'category',
			axisTick:{
				alignWithLabel:true
			},
			data:['2010','2011','2012','2013','2014','2015','2016']
		}
	],
	yAxis:[{
		type:'value',
		name:'Chengdu',
		min: 0,
		max: 80000,
		position:'right',
		axisLine:{
			lineStyle:{
				color:'#5793f3'
			}
		},
		axisLabel:{
			formatter:'{value}'
		}
		},
		{type:'value',
		name:'Sichuan',
		min: 0,
		max: 80000,
		position:'right',
		offset:80,
		axisLine:{
			lineStyle:{
				color:'#d14a61'
			}
		},
		axisLabel:{
			formatter:'{value}'
		}
		},
		{type:'value',
		name:'Per capita GDP',
		min: 0,
		max: 80000,
		position:'left',
		axisLine:{
			lineStyle:{
				color:'#675bba'
			}
		},
		axisLabel:{
			formatter:'{value}'
		}
		}
	],
	series:[
	{
		name:'Average wage of Chengdu',
		type:'bar',
		data:[
		30515,
		34008,
		38221,
		48358,
		51681,
		56872,
		61330
		]
	},
	{
		name:'Average wage of Sichuan',
		type:'bar',
		yAxisIndex:1,
		data:[
		26952,
		31489,
		35873,
		41795,
		45697,
		50466,
		54425
		]
	},
	{
		name:'Per capita GDP of Chengdu',
		type:'line',
		yAxisIndex:2,
		data:[
		41253,
		49438,
		57624,
		63977,
		70019,
		74273,
		76960
		]
	}
	]
}
```



## Rapid urban expansion:The microcosm of urbanization of China

### Population
The Population of Chengdu in 2009 was 9339734, increasing at an average annual rate of 6.8%
since 2000. Although the increase speed has slowed down since 2010, its population annual increase rate is much higher than those of Asia and the world.
					
<table width="800" style="margin-left: auto; margin-right: auto;">
        <tr>
            <td width="400">
```chart
{
    title: {
        text: 'Population',
		subtext:'Million'
    },
    tooltip: {
        trigger: 'axis'
    },
    legend: {
		x: "20%",
		top: '10%',
        data:['Chengdu Population']
    },
    toolbox: {
        show: true,
        feature: {
            dataZoom: {
                yAxisIndex: 'none'
            },
            dataView: {readOnly: false},
            magicType: {type: ['line', 'bar']},
            restore: {},
            saveAsImage: {}
        }
    },
	settings: {
	width: '100%',
	height: '300px'
  },
    xAxis:  {
        type: 'category',
        boundaryGap: false,
        data: ['1988','2000','2009','2017']
    },
    yAxis: {
        type: 'value',
        axisLabel: {
            formatter: '{value} '
			
        }
		
    },
    series: [
        {
            name:'Population',
            type:'line',
            data:[2.019420,5.117629,9.339734,14.353300],
        
    }]
}
```
            </td>
            <td width="400">
```chart
{
    title: {
        text: 'Population Avg Change'
    },
    tooltip: {
        trigger: 'axis',
        axisPointer: {
            type: 'shadow'
        }
    },
    legend: {
        data: ['1988-2000', '2000-2009', '2010-2018'],
		x: "2%",
		top: '10%'
    },
    grid: {
        left: 100
    },
    toolbox: {
        show: true,
        feature: {
            saveAsImage: {}
        }
    },
		settings: {
	width: '100%',
	height: '300px'
  },
    xAxis: {
        type: 'value',
        name: '%',
        axisLabel: {
            formatter: '{value}'
        }
    },
    yAxis: {
        type: 'category',
        inverse: true,
        data: ['Chengdu', 'East Asia', 'World'],
        axisLabel: {
            formatter: function (value) {
                return '{' + value + '| }\n{value|' + value + '}';
            },
            margin: 20,
            rich: {
                value: {
                    lineHeight: 30,
                    align: 'center'
                },
                Sunny: {
                    height: 40,
                    align: 'center'
                },
                Cloudy: {
                    height: 40,
                    align: 'center'
                },
                Showers: {
                    height: 40,
                    align: 'center'
                  
                }
            }
        }
    },
    series: [
        {
            name: '1988-2000',
            type: 'bar',
            data: [7.7, 3.4, 4.5],
        },
        {
            name: '2000-2009',
            type: 'bar',
            data: [6.8, 3.4, 4.5]
        },
        {
            name: '2010-2018',
            type: 'bar',
            data: [2.21,1.03,1.21]
        }
    ]
}
```
            </td>
        </tr>
    </table>

### Moving To Chengdu!
<table width="800" style="margin-left: auto; margin-right: auto;">
        <tr>
            <td width="400">
```chart
{
	backgroundColor:'',
	title:{
	textStyle:{
		fontWeight:'normal',
		fontSize:16
	},
	left:'6%'
	},
	tooltip:{
		trigger:'axis',
		axisPointer:{
			lineStyle:{
					color:'#57617B'
			}
		}
	},
	legend:{
		icon:'rect',
		itemWidth:14,
		itemHeight:5,
		itemGap:13,
		data:['Belief Index of Development in Chengdu','Happiness Index of Living in Chengdu'],
		right:'10%',
		textStyle:{
			fontSize:12
		}
	},
	grid:{
		left:'3%',
		right:'10%',
		bottom:'3%',
		containLabel:true
	},
	xAxis:[{
		type:'category',
		boundaryGap:false,
		axisLine:{
			lineStyle:{
				color:'#57617B'
			}
		},
		data:['2013','2016']
	}],
	yAxis:[{
		type:'value',
		axisTick:{
			show:false
		},
		axisLine:{
			lineStyle:{
				color:'#57617B'
			}
		},
		axisLabel:{
			margin:10,
			textStyle:{
				fontSize:14
			}
		},
		splitLine:{
			lineStyle:{
				color:'#57617B'
			}
		}
	}],
	series:[{
		name:'Belief Index of Development in Chengdu',
		type:'line',
		smooth:true,
		lineStyle:{
			normal:{
				width:1
			}
		},
		areaStyle:{
			normal:{
				color: new echarts.graphic.LinearGradient(0,0,0,1,[{
					offset:0,
					color:'rgba(137,189,27,0.3)'
				},{
					offset:0.8,
					color:'rgb(137,189,27,0)'}],false
				),
				shadowColor:'rgba(0,0,0,0.1)',
				shadowBlur:10
			}
		},
		itemStyle:{
			normal:{
				color:'rgb(137,189,27)'
			}
		},
		data:[36.15,49.89]
		},
		{
		name:'Happiness Index of Living in Chengdu',
		type:'line',
		smooth:true,
		lineStyle:{
			normal:{
				width:1
			}
		},
		areaStyle:{
			normal:{
				color: new echarts.graphic.LinearGradient(0,0,0,1,[{
					offset:0,
					color:'rgba(219,50,51,0.3)'
				},{
					offset:0.8,
					color:'rgb(219,50,51,0)'}],false
				),
				shadowColor:'rgba(0,0,0,0.1)',
				shadowBlur:10
			}
		},
		itemStyle:{
			normal:{
				color:'rgb(219,50,51)'
			}
		},
		data:[50.66,68.63]
		}
		]
}
```
            </td>
            <td width="400">

```chart
{
	title:{
		top:'45%',
		left:'center',
		text:'Most liked City',
		textStyle:{
			color:'#fff',
			fontStyle: 'normal',
			fontWeight:'normal',
			fontSize:14
		},
		subtext:'Chengdu' + ' '+ (0.2894*10000/100).toFixed(2) + '%',
		subtextStyle:{
			color:'#fff',
			fontSize:12
		}
	},

	series:[{
		type:'liquidFill',
		itemStyle:{
			normal:{
				opacity: 0.4,
				shadowBlur:0,
				shadowColor:'blue'
			}
		},
		name:'Chengdu',
		data:[{
			value: 0.6,
			itemStyle:{
				normal:{
					color:'#53d5ff',
					opacity:0.6
				}
			}
	}],
	color:['#53d5ff'],
	center:['50%','50%'],
	label:{
		normal:{
			formatter:'',
			textStyle:{
				fontSize:12
			}
		}
	},
	outline:{
		itemStyle:{
			borderColor:'#86c5ff',
			borderWidth: 0
		},
		borderDistance: 0
	}
	},
	{
		type:'pie',
		radius:['42%','50%'],
			color:['#c487ee','#deb140','#49dff0','#034079','#6f81da','00ffb4'],
		hoverAnimation:false,
		label:{
			show:true,
			normal:{
				formatter:'{b}\n{d}%',
				show:true,
				position:''
			},
		},
		labelLine:{
			norma:{
				show:false
			}
		},
		
		itemStyle:{
			normal:{
				borderWidth:2,
				borderColor:'#fff',
			},
			emphasis:{
				borderWidth:0,
				shadowBlur:2,
				shadowoffsetX:0,
				shadowColor:'rgba(0,0,0,0.5)'
			}
		},
		data:[
		{value:0.224,name:'Chengdu'},
		{value:0.201,name:'Hangzhou'},
		{value:0.081,name:'Suzhou'},
		{value:0.078,name:'Xiamen'},
		{value:0.065,name:'Nanjing'},
		{value:0.047,name:'Qingdao'},
		{value:0.041,name:'Chongqing'},
		{value:0.037,name:'Wuhan'}
		]
	}]
}

```
            </td>
        </tr>
    </table>


```chart
{
	tooltip:{},
	toolbox:{
		show:false
	},
	title: {
        text: 'Sense Index of career development in Chengdu'
    },
	series:[{
		name:"People living in Chengdu",
		type:'gauge',
		z:3,
		min:0,
		max:100,
		splitNumber:10,
		radus:'60%',
		axisLine:{
			lineStyle:{
				width:3
			}
		},
		axisTick:{
			length:1,
			lineStyle:{
				color:'auto'
			}
		},
		splitLine:{
			length:10,
			lineStyle:{
				color:'auto'
			}
		},
		axisLabel:{},
		title:{
			fontWeight:'bolder',
			fontSize: 20,
			offsetCenter:[0,'80%']
		},
		pointer:{
			width:3
		},
		detail:{
			fontSize:20,
			offsetCenter:[0,'65%']
		},
		data:[{
			value: 84.58,
			name:'People In Chengdu'
		}]
	},
	{
		name:"People in first-tier cities",
		type:'gauge',
		center:['80%','55%'],
		min:0,
		max:100,
		startAngle:135,
		endAngle:-45,
		splitNumber:5,
		radus:'45%',
		axisLine:{
			lineStyle:{
				width:2
			}
		},
		axisTick:{
			length:1,
			lineStyle:{
				color:'auto'
			}
		},
		splitLine:{
			length:8,
			lineStyle:{
				color:'auto'
			}
		},
		title:{
			fontSize: 20,
			offsetCenter:[0,'80%']
		},
		pointer:{
			width:2
		},
		detail:{
			fontSize:20,
			offsetCenter:[0,'65%']
		},
		data:[{
			value: 43.37,
			name:'People in second-tier cities'
		}]
	},{
		name:"People in first-tier cities",
		type:'gauge',
		center:['20%','55%'],
		min:0,
		max:100,
		endAngle:45,
		splitNumber:5,
		radus:'45%',
		axisLine:{
			lineStyle:{
				width:2
			}
		},
		axisTick:{
			length:1,
			lineStyle:{
				color:'auto'
			}
		},
		splitLine:{
			length:8,
			lineStyle:{
				color:'auto'
			}
		},
		title:{
			fontSize: 20,
			offsetCenter:[0,'80%']
		},
		pointer:{
			width:2
		},
		detail:{
			fontSize:20,
			offsetCenter:[0,'65%']
		},
		data:[{
			value: 53.54,
			name:'People in first-tier cities'
		}]
	}
	]
}
```
	


## Businesses
### Overview

test1

<iframe   src="https://feiyuxiaothu.github.io/Exploration-of-Chengdu-Landscope/Charts/ImportandSales.html" width="100%" height="450px"   frameborder="1/0"     scrolling="no">  
</iframe>

### 1

test 2

<iframe   src="https://feiyuxiaothu.github.io/Exploration-of-Chengdu-Landscope/Charts/Tertiary.html" width="100%" height="450px"   frameborder="1/0"     scrolling="no">  
</iframe>

### 2

test 3

<iframe   src="https://feiyuxiaothu.github.io/Exploration-of-Chengdu-Landscope/Charts/Finance&Real_Estate.html" width="100%" height="450px"   frameborder="1/0"     scrolling="no">  
</iframe>

### Efficency of tranportation

test 4

<iframe   src="https://feiyuxiaothu.github.io/Exploration-of-Chengdu-Landscope/Charts/Commuting%20time.html" width="100%" height="450px"   frameborder="1/0"     scrolling="no">   
</iframe>

### What about tech? 
#### A short look at the taxi industry.
<iframe   src="https://feiyuxiaothu.github.io/Exploration-of-Chengdu-Landscope/Charts/keplerChengduTaxi.html" width="100%" height="450px"   frameborder="1/0"     scrolling="no">   
</iframe>

### Overview

## But Chengdu is big

### Living and Working 

<iframe   src="https://feiyuxiaothu.github.io/Exploration-of-Chengdu-Landscope/Charts/WorkingDensity.html" width="100%" height="500px"   frameborder="1/0"     scrolling="no">   
</iframe>

<iframe   src="https://feiyuxiaothu.github.io/Exploration-of-Chengdu-Landscope/Charts/PyramidDensity.html" width="100%" height="420px"   frameborder="1/0"     scrolling="no">   
</iframe>
 
### Let's take a look at housing. 

The following figure exhibits the general house sales data in Chengdu.

```chart
option = {
    color: ['#5793f3','#d14a61'],
	tooltip:{
		trigger:'axis',
		axisPointer:{type:'cross'}
	},
	toolbox:{
		feature:{
			dataView:{show:true,readOnly:false},
			restore:{show:true},
			saveAsImage:{show:true}
		}
	},    
    legend:{
        data:['house price (RMB/m2)', 'sales area (10,000m2)']
    },
    xAxis: {
        type: 'category',
        axisTick:{
            alignWithLabel:true
        },
        data: ['2009', '2010', '2011', '2012', '2013', '2014', '2015', '2016', '2017']
    },
	yAxis:[{
		type:'value',
		name:'house price',
		min: 0,
		max: 9000,
		position:'left',
		axisLine:{
			lineStyle:{
				color:'#5793f3'
			}
		},
		axisLabel:{
			formatter:'{value}'
		}
		},
		{type:'value',
		name:'sales area',
		min: 0,
		max: 3500,
		position:'right',
		axisLine:{
			lineStyle:{
				color:'#d14a61'
			}
		},
		axisLabel:{
			formatter:'{value}'
		}
		}
		
	],
	series:[
	{
		name:'house price (RMB/m2)',
		type:'line',
		data:[
		4864.00,
		5827.00,
		6360.89,
		6678.46,
		6708.00,
		6536.00,
		6584.00,
		7377.00,
		8595.00
		]
	},
	{
		name:'sales area (10,000m2)',
		type:'line',
		yAxisIndex:1,
		data:[
		2547.59,
		2289.92,
		2284.91,
		2424.61,
		2555.81,
		2476.25,
		2447.13,
        3279.17,
        2976.47
		]
	},
	]
}
```

We compare the unit house price with other second-tier cities: Chongqing, Xi'an and Wuhan from 2010 to 2019.
<iframe   src="https://feiyuxiaothu.github.io/Exploration-of-Chengdu-Landscope/Charts/area-basic.html" width="1200px" height="600px"   frameborder="1/0" scrolling="yes">   
</iframe>

We also visualize the unit house price in each district and its trend from 2010 to 2019.
<iframe   src="https://feiyuxiaothu.github.io/Exploration-of-Chengdu-Landscope/Charts/map-chengdu.html" width="100%" height="600px"   frameborder="1/0">   
</iframe>


## Data Sources

### Data from government
<span style="font-size: 20px; font-weight: 600">National Bureau of Statistics</span> has made its database public. We can get access to the GDP data, the Industrial index and housing price data of Chengdu, and also we can get the data of other cities for comparision.

Here is the National database:
http://data.stats.gov.cn/index.htm

Chengdu government provides datasets of several aspects, such as transportation data, housing data and
employment data. And we can get access to almost all aspects of this city through the database.

Here is the Chengdu public data open platform.
http://www.cddata.gov.cn/odweb/index.htm.


Futhermore, we have access to the Statistical yearbook of Chengdu and Sichuan Province, which are
available at :
http://www.cdstats.chengdu.gov.cn/htm/detail_123764.htmlandhttp://tjj.sc.gov.cn/tjcbw/tjnj/2017/zk/indexch.htm.

### Data from other platforms

<span style="font-size: 20px; font-weight: 600">Housing data</span>: Anjuke is a website with rich and real-time real estate data, and we can easily get historical prices or compare prices in different regions via its API interface of the website :
https://www.anjuke.com/fangjia/.

<span style="font-size: 20px; font-weight: 600">Employment</span>: Lagou is a platform for job seekers, so we can get the supply and demand data in the job market which can help us to analyze the industry development and economic expectations. The Lagou
website is:
https://www.lagou.com/gongsi/252-0-0-0

<span style="font-size: 20px; font-weight: 600">Note</span>: Filtered data is available at our project repository:
[Exploration of Chengdu Landscope](https://github.com/feiyuxiaoThu/Exploration-of-Chengdu-Landscope)

## Tools

[Mapbox](https://www.mapbox.com/) To make map     &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;           [Kepler.gl](https://kepler.gl/) To make map data visualization

[Echarts.js](https://echarts.baidu.com/) To make various charts &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;  [Highcharts.js](https://www.highcharts.com/) Also to make interactive charts

[Geojson.io](http://geojson.io) To process json files &emsp;&emsp;&emsp;&emsp;&emsp;&emsp; &emsp;    [Docsify](https://github.com/docsifyjs/docsify/) A magical documentation site generator

## About Us
Our names are [Xiao Feiyu](https://github.com/feiyuxiaothu), [Fang Xiaonan](https://github.com/fornorp) and [Zhang Yusheng](https://github.com/x2yszzz).

This project was created for the 2019Spring course : Data Visualization, at the Department os Computer Science within Tsinghua University.

Special thanks to our professor: Prof. Zhang Songhai




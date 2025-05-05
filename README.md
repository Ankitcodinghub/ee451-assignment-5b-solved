# ee451-assignment-5b-solved
**TO GET THIS SOLUTION VISIT:** [EE451 Assignment 5b Solved](https://www.ankitcodinghub.com/product/ee451-assignment-5b-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;100477&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE451 Assignment 5b Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
1. Examples

Copy example files to your home directory.

1. Login to HPC 2. Copy

cp -r /project/xuehaiqi_652/cuda .

The hello.cu contains the CUDA implementation of HelloWorld.

<ol>
<li>Login to HPC</li>
<li>Setup MPI toolchain:</li>
<li>Compile
nvcc -O3 hello.cu
</li>
<li>Run
The option -t specifies the limit of run time. Setting it as a small number will get your program scheduled earlier. The option –mem specifies the minimum memory requirement. Setting it as a small number will get your program scheduled earlier. However, you need it when you run sumArraysOnGPU and sumMatrixOnGPU. For more information on srun options, you can use man srun to find out.
</li>
<li>Profile (optional)
srun -n1 –gres=gpu:p100:1 –partition=debug nvprof ./a.out
</li>
<li>Allocate a machine</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
module purge

module load gcc /8.3.0 cuda /10.1.243

</div>
</div>
<div class="layoutArea">
<div class="column">
srun -n1 –gres=gpu:1 –mem=16G -t1 ./a.out

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
salloc -n1 –gres=gpu:1 –mem=16G -t10

// After the allocation, you will log on the machine and have 10 minutes to perform multiple operations

./a.out

// edit , compile , and run again without waiting for a new allocation

./a.out ./a.out

</div>
</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
2. (40 points) In reduceInteger.cu, refer to the kernel reduceUnrolling8 and replace the following code segment:

</div>
</div>
<div class="layoutArea">
<div class="column">
PA5b— Spring 2021

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
// unrolling 8

int a1 = g_idata[idx]; int a2 = g_idata[idx + int a3 = g_idata[idx + int a4 = g_idata[idx + int b1 = g_idata[idx + int b2 = g_idata[idx + int b3 = g_idata[idx + int b4 = g_idata[idx +

</div>
<div class="column">
blockDim.x];

2 * blockDim.x]; 3 * blockDim.x]; 4 * blockDim.x]; 5 * blockDim.x]; 6 * blockDim.x]; 7 * blockDim.x];

</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
with the functionally equivalent code below:

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
int *ptr = g_idata + idx;

int tmp = 0;

// Increment tmp 8 times with values strided by blockDim.x for *int i = 0; i &lt; 8; i++) {

tmp += *ptr;

ptr += blockDim.x; }

g_idata[idx] = tmp;

</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
Compare the performance.

<ol start="3">
<li>(30 points) Refer to the kernel reduceInterleaved and the kernel reduceCompleteUnrollWraps8 and implement a version of each for floats. Compare their performance and explain

any differences (profiling with nvprof is optional). Are there any differences compared

to operating on integer data types?</li>
<li>(30 points) Refer to the file nestedHelloWorld.cu and implement a new kernel using the methods illustrated in Figure 3-30 (Change igrid to 2; Only one thread calls the kernel recursively). To compile it, add the following options.
nvcc -O3 -arch=sm_35 -rdc=true hello.cu
</li>
</ol>
</div>
</div>
</div>

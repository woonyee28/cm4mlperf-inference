This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/cm4mlops).

*Check [CM MLPerf docs](https://docs.mlcommons.org/inference) for more details.*

## Host platform

* OS version: Linux-6.1.110-1.el9.elrepo.x86_64-x86_64-with-glibc2.34
* CPU version: x86_64
* Python version: 3.10.15 (main, Oct  3 2024, 07:27:34) [GCC 11.2.0]
* MLCommons CM version: 3.2.4

## CM Run Command

See [CM installation guide](https://docs.mlcommons.org/inference/install/).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo mlcommons@cm4mlops --checkout=5aeaffdca72142871dcde95ebf8a37e65fe3e06e

cm run script \
	--tags=run-mlperf,inference,_r4.1-dev \
	--model=bert-99 \
	--implementation=reference \
	--framework=pytorch \
	--category=edge \
	--scenario=Offline \
	--execution_mode=valid \
	--device=cuda \
	--quiet
```
*Note that if you want to use the [latest automation recipes](https://docs.mlcommons.org/inference) for MLPerf (CM scripts),
 you should simply reload mlcommons@cm4mlops without checkout and clean CM cache as follows:*

```bash
cm rm repo mlcommons@cm4mlops
cm pull repo mlcommons@cm4mlops
cm rm cache -f

```

## Results

Platform: scc104_gpu0.novalocal-reference-gpu-pytorch-cu122

Model Precision: fp32

### Accuracy Results 
`F1`: `90.87487`, Required accuracy for closed division `>= 89.96526`

### Performance Results 
`Samples per second`: `47.9697`
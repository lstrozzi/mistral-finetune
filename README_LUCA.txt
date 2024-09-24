# This global variable must be run, in order to enable the NVIDIA CUDA GPU on a local machine:
export CUDA_VISIBLE_DEVICES=0

# must also run:
conda install pytorch

# the only way to work is:
python -m torch.distributed.run --nproc-per-node 1 -m train example/7B.yaml

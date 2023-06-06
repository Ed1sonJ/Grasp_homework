# Grasp homework for computer architecture
代码参考 https://github.com/faldupriyank/grasp

本代码仅作作业使用

# 运行
1. 设置环境变量

export DBG_ROOT='directory where this repo is cloned'

cd ${DBG_ROOT}/trace-based-simulators

2. 修改trace-based-simulators/Makefile，去选择运行的dataset，执行下述命令

make clean; make POLICY=grasp;

# VNT101 FEP+ 输入包（复旦服务器）

流感 NP (9OUG) + 31 配体（VNT101 参考 + 30 LXH）相对结合自由能，固定 FEP 图 47 边全连通。
受体 = PrepWizard 完整优化版；配体 = LigPrep + Glide XP pose；全中性无电荷校正腿。

## 用法（在装好薛定谔 2026-2 的机器上）

```bash
tar xzf vnt101_fep31_fudan_package.tar.gz && cd package
./00_install_schrodinger.sh   # 若薛定谔未装（自动找 rar/便携包）
./01_run_fep.sh               # 跑 FEP（守护+断点续跑）；SIM_TIME=2000 可改 2ns
./01_run_fep.sh status        # 进度
./02_extract_results.sh       # 完成后出 ΔG 排名表
./03_run_in_docker.sh         # 或用 docker 镜像方式（vnt101_fep31_image.tar）
```

Docker 镜像（13.6GB，含 ubuntu22.04+薛定谉+本包）因超出 GitHub 单文件限制未入库，
另行传输；license 不锁机器（2050 年有效）。

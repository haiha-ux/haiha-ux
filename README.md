### Hi, I'm Hai — I make computer vision run on real hardware

Computer Vision & Edge AI engineer in Ho Chi Minh City, Vietnam. I lead an AI team building perception for UAVs, and I care about the part after the notebook: getting a model to run fast and correctly on a drone, a Jetson, an NPU or an FPGA.

**What I work on**
- **Edge deployment** — PyTorch → ONNX → TensorRT (Jetson), Qualcomm NPU (QNN/QAIRT), Xilinx Vitis-AI; INT8/INT16 quantization with accuracy checks before and after
- **Multi-camera geometry** — fisheye/stereo calibration (intrinsics, extrinsics, camera–IMU), synchronised capture, 360° depth for obstacle avoidance
- **Vision pipelines** — detection, tracking, segmentation; GStreamer/RTSP multi-camera streaming
- **Robot learning** — running and evaluating VLA policies (LeRobot, LIBERO)
- **Hardware** — KiCad schematic/PCB, 2D CAD drafting (DXF/DWG), RTL (SystemVerilog/Verilog), Tiny Tapeout ASIC design, FPGA CNN accelerators

**Selected public work**
| Repo | What |
|---|---|
| [yolo-tensorrt-edge](https://github.com/haiha-ux/yolo-tensorrt-edge) | YOLO → ONNX → TensorRT FP32/FP16/INT8 with a reproducible latency vs COCO-accuracy benchmark |
| [camera-calibration-report](https://github.com/haiha-ux/camera-calibration-report) | Pinhole, fisheye and stereo calibration with held-out reprojection/epipolar error on public data |
| [object-tracking-bench](https://github.com/haiha-ux/object-tracking-bench) | YOLO11 + ByteTrack/BoT-SORT on MOT17 with HOTA/MOTA/IDF1, PyTorch vs TensorRT FP16, per-track speed |
| [libero-vla-repro](https://github.com/haiha-ux/libero-vla-repro) | Reproduction of SmolVLA (flow matching) vs pi0-FAST (tokenized actions) on LIBERO, with CIs, latency and a gap-vs-paper analysis |
| [pcb-sample-preamp](https://github.com/haiha-ux/pcb-sample-preamp) | 2-channel 48V phantom-powered mic preamp (INA163): KiCad schematic, hand-routed 2-layer PCB, ERC/DRC clean, BOM, Gerbers |
| [cad-sample-tests](https://github.com/haiha-ux/cad-sample-tests) | 2D CAD drafting: ISO mechanical part drawing (3 views, section A-A, tolerances) and a 1:50 floor plan, delivered as DXF/DWG/PDF |
| [ttihp-snn-ascon](https://github.com/haiha-ux/ttihp-snn-ascon) | NIST Ascon-128 AEAD crypto core in Verilog for the Tiny Tapeout IHP 26a shuttle (130 nm, ~6K cells) |
| [circuit-op](https://github.com/haiha-ux/circuit-op) | Automatic circuit discovery with graph neural networks and reinforcement learning |
| [electric-fox](https://github.com/haiha-ux/electric-fox) | Electric VLSI design system fork: 3D visualisation, analog layout synthesis, Java 17 |
| [verdict-prereg](https://github.com/haiha-ux/verdict-prereg) | Pre-registered study: label-free threshold re-setting under image shift |

**In the field**
- AI engineer in a city-scale drone pilot with Hanoi Police for traffic and urban-order monitoring (2026) — [Lao Động](https://news.laodong.vn/xa-hoi/tuan-tra-bang-uav-buoc-tien-huong-toi-do-thi-an-toan-hien-dai-1742963.ldo), [An ninh Thủ đô](https://anninhthudo.vn/cong-an-ha-noi-tuan-tra-bang-uav-make-in-viet-nam-dot-pha-quan-tri-giao-thong-va-trat-tu-do-thi-post660666.antd)
- Co-author, *MARS* — lightweight multi-task Mamba model for mapless UAV navigation (IAAA 2026, Springer LNNS)
- M.Eng. candidate, Electronics Engineering, Ho Chi Minh City University of Technology

**Tools** Python · C/C++ · PyTorch · TensorRT · ONNX Runtime · OpenCV · QNN/QAIRT · CUDA · ROS 2 · PX4 · Docker · SystemVerilog · KiCad · LeRobot

I'm Hai, an engineer in Ho Chi Minh City. Most of my work is getting vision models to run correctly and fast on the hardware they will actually ship on. At my day job I work on perception for UAVs: multi-camera fisheye calibration, depth for obstacle avoidance, and quantized models on Qualcomm NPUs. I'm also doing an M.Eng. in electronics at Ho Chi Minh City University of Technology.

The repos below are things I built to measure something properly. Each one has the raw numbers, the commands to reproduce them, and a section on what didn't work.

| Repo | What it measures |
|---|---|
| [multistream-trt-pipeline](https://github.com/haiha-ux/multistream-trt-pipeline) | Several RTSP cameras into one GPU: hardware decode, batched TensorRT YOLO, a tracker per camera. Latency per stage and total FPS from 1 to 12 streams. |
| [ros2-trt-detector](https://github.com/haiha-ux/ros2-trt-detector) | A ROS 2 node that runs a TensorRT detector on a camera topic. Holds 30 Hz at 640 and 1280 input, 14 to 19 ms from image stamp to detections. |
| [yolo-tensorrt-edge](https://github.com/haiha-ux/yolo-tensorrt-edge) | YOLO exported to ONNX and TensorRT at FP32, FP16 and INT8, with latency against COCO accuracy for each. |
| [object-tracking-bench](https://github.com/haiha-ux/object-tracking-bench) | ByteTrack and BoT-SORT on MOT17, scored with HOTA, MOTA and IDF1, PyTorch against TensorRT. |
| [camera-calibration-report](https://github.com/haiha-ux/camera-calibration-report) | Pinhole, fisheye and stereo calibration, judged on held-out images rather than the training error. |
| [libero-vla-repro](https://github.com/haiha-ux/libero-vla-repro) | Two robot policies (SmolVLA and pi0-FAST) re-run on the LIBERO benchmark, with confidence intervals and an honest look at why one fell short of its paper. |
| [pcb-rp2040-usbc](https://github.com/haiha-ux/pcb-rp2040-usbc) | A four-layer RP2040 board with USB-C, a 90 ohm USB pair and JLCPCB fab files, plus a 2x2 panel and a DFM check against the fab's published limits. |
| [pcb-sample-preamp](https://github.com/haiha-ux/pcb-sample-preamp) | A two-channel phantom-powered microphone preamp in KiCad, checked against the TI datasheet, with hand-routed inputs and fab files. |
| [eagle-to-kicad-qwiic-button](https://github.com/haiha-ux/eagle-to-kicad-qwiic-button) | An open-source Eagle board (SparkFun Qwiic Button, CC BY-SA) migrated to KiCad 10, with every net and copper segment checked against the original. |
| [cad-sample-tests](https://github.com/haiha-ux/cad-sample-tests) | A mechanical part drawing, a 1:50 floor plan, and a 1921 scanned drawing redrawn to its printed dimensions and overlaid on the original, delivered as DXF, DWG and PDF. |
| [ttihp-snn-ascon](https://github.com/haiha-ux/ttihp-snn-ascon) | An Ascon-128 crypto core in Verilog, submitted to the Tiny Tapeout IHP 26a shuttle (130 nm). |

Outside of these: in 2026 I was the AI engineer on a city-scale drone pilot for traffic and urban-order monitoring in Hanoi ([Lao Động](https://news.laodong.vn/xa-hoi/tuan-tra-bang-uav-buoc-tien-huong-toi-do-thi-an-toan-hien-dai-1742963.ldo), [An ninh Thủ đô](https://anninhthudo.vn/cong-an-ha-noi-tuan-tra-bang-uav-make-in-viet-nam-dot-pha-quan-tri-giao-thong-va-trat-tu-do-thi-post660666.antd)), and I co-authored MARS, a small multi-task Mamba model for mapless UAV navigation (IAAA 2026, Springer LNNS).

Day to day I use Python and C++, PyTorch, TensorRT, ONNX Runtime, OpenCV, CUDA, GStreamer, ROS 2 and KiCad.

# 🦷 Attention is All You Need (for Teeth): Discovering Dental Structure with SetVAE

## 🚀 Overview

This project brings **state-of-the-art set-based generative modeling** into 3D medical vision by adapting **SetVAE (CVPR 2021)** to dental geometry.

We transform full jaw meshes into point sets and train a **hierarchical attention-based VAE** to learn structure directly from raw geometry.

> **Goal:** Can a generative model *discover individual teeth* without any supervision?

---

## 🧠 Why This Matters

* Moves beyond supervised segmentation
* Explores **unsupervised structure discovery** in 3D
* Leverages **attention as an interpretable signal**
* Connects **generative modeling + medical geometry + set learning**

👉 This sits at the intersection of **modern CV (transformers, attention)** and **3D understanding**

---

## 🧬 Method

* Convert each jaw into a **set of 3D points**
* Train SetVAE to model the distribution of these sets
* Extract **hierarchical encoder attention**
* Interpret attention as **soft clustering**
* Compare clusters with **ground-truth tooth instances**

---

## 🧪 Results

### 🟢 Ground Truth vs Reconstruction

![Image](https://images.openai.com/static-rsc-4/BJJD2aoxSQUlv02LiJhJ5JZb0C4oDZuSVM-CoduemchNXV9KEcGL3MqgXWCJb3vKRbZdt8ByqRxe5y6NSJRQcdJgTJbsa2fv0E1eHfSB9ozpT9Y2raqoGNk3xEb-bIWJePUDqtwTvUL0ftLv-OOGgbO7_BPYCOzfDCCokT8sPBXyFU4Iy2W7tGSbJQnaw29y?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/pYtNGph14fXEEedbNCR3WBBvI6mZ2ToYL-6T_-Ek7Hu_CvbRMscNQFWiPWjhzp93_75vmAn5RewF53e1fvemb0DHmFVSwDGUP5_Jqvib6mjsQYGyz1lqhNoFNnRvLWl1D3oCHSDl_I-RXrnlRhxhMfAtmi0xOaN6_eEFz7Taj3r4usTSiCPlj_n2ipRXide1?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Ej9xGbWCAzPJTOs0eVy57vjHqfGQeK9l_hIqNWmkwbeveJjZi9ZmGcnb-g-dqkEeZJUDQAthoU7-wgbCLBeqS50CQ2EIPlcqktm50eyQiM7l2mCFlnaoPPul9XI-MVtSRRa-ys5hkZ66_rhhUh0DJtFQCK92p18co3_fPgozure9QlJYPVIo6LacHgK4yUQN?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/yw7RRGPpIHUkd-kbsugKGafOSO6TrMtTLqTKx6ERepDocO63bVH3FBwAJ3w4oyaimRiWZyO45dscGb85Q60o3UfQmXAcF90Ox1snrTj6ytLNLCzf_0wdLKd8rp5W7TIKo5ZHwjfl_Quv_WExtj8etV7X_3O_mfj5wuHY8-8IGEKWHX29xnAEgGI5lizGpuP7?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/6cPaoot-ky1UXRnhC2t8vzW2XV3iTadrmFUXlavMmFCeah8OZZ1IlbgzssFFsDDJxpxZorC5Uewuc0fXju7r_OU9h-j533e6L5ZmPXVZExeEOWLe4LZ0TOoFFFeTmpiAZkomC2zF6tayN3Vp6OlQb_48KfEGwWZTLe3zPebqGHKfYaky3NLHxagym3MoGJqS?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/p2E9t_KBaKzbtWHVyJDQxQEtL7U0UHh5bFsEdJLZzQH5Hvedu3oGNxPkgsLbj8LYnNmSdvWNfHrI-GeLha64C5CoAp1ErZ51Tlm4BSGoixmt8K6ELwhwkgKkl0RKsymbUIzoicDxaCyj64pdlFyHI8RIdtGzSz_VvrMR-_PCLR1H6BIyIo4xVSvq8tSOr84d?purpose=fullsize)

* SetVAE successfully reconstructs complex dental geometry
* Preserves global jaw shape and local tooth structure
* Demonstrates strong generative capacity on unordered 3D sets

---

### 🔵 Encoder Attention = Tooth Discovery

![Image](https://images.openai.com/static-rsc-4/f03tQV-3CPZx4UyQ6im7ccVYQ0aZsqt-HW9NAsAZlWCcRjwVVfSxIfo5-1Ugji3snYiNA1Ch7Ts4_iVlnEEE4SFK-XQ9kqkdJmi-JCGCx5YJxqHfz4kTo-vxPgXuurCI3TuPVXtaSPad5uxKvo-44LfbuQxc0ynNdqTlT0SKTIxSMJ4Mc2X0CI9ckmJYpRMb?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/vncYEMnzAUJQ2FWd7Zs65y2s-FjDNEVCvmjg9BplshRFIu9gOK4BS7jPbxBSDiIagMv9QCwQu-kYgpj2i9mxwG5zZPZh0wbdtVR3H91cObHpD88h4TXPsTUaUBJGLGAFDlaxRJ7hwi_wzVt3DUP20eQjX95ITLKazO3MUh3PS_Ho3wm2s22HuxooCbl1NN6_?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/8gUmGFZZI0otj9oFs2FfoEObXHgb6bEYWXE9SpMEW_wF6gFTca0Bd74QkRQHNHbVCWoZKhKN2uPcUgWJwdvYhWrgCWDNNIHYEdOwqNyzcLk1uXgq5zPelBBNgKESFIO59TZFe36oVLTWZBGQSskgEoyr9WACbyGZ-VgdCRzBTKEKJZRLqACBg1lun7iaqMce?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/UyGtamCq0sspGgRShvKqM6DRV8l1Fgi6gyt8LYWKzey-tIMy0ef9ezELMPrf1rFnT-8ox7jazGQT42W9DVHPeVizGldhDiJFHrR_Tv7Ea1h38B7_EzjWSM7T2sPLs_gcP487PXl6bhwLPWicX-RZivNrGYn2CsX-_rnd-K7ppc_0YLLqsf6UDWm97sWsPXot?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/uToTc3BKS9D7Pf-CLD7c1TIXDGN66IQrt1HnpA--jBKDEP8C2YhPKMBsQ1OqqxUIjIyVdxMwSJwXXG2aPb9JO8VGattFOozxfuesSGrshR8YfMQfQp2vwEP9qC9YylQozWLQshN5wv8ncBDrnzMkUuijXs6qWaBAgbQgrpAF-a7GHME87vj-GcvncOvmbU9b?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/oFwRed8uqU8dzkXJXXb2Jb_QARg3eo1CL5fxblgFsvnt6MFdcZyqMYVmLud8DJVbKu1i7iuwFhI6qPf-L0bdUj8sDTloOeQu3JYwTTnd8eHRVj0UJUkR2WJFRjVRSwvTM26kzituh14oDEuIJhTgbxDIR3e4wckxyO722n2OUJnNT2dHMTOF_4l3Ga8ST2DL?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/twlx8xsZi7_oP0D-_c-yjtMPNPxUn_IgpfINBqoT9JKIE36YCR5qRKYPDQqGCyVBqGK1M_nQDO383UZ9UBQZqmffp2L_ZeH-LZkpt57toQZxyBen4V3jrYgk6YteST4O5_GBzC2IGr4y_ke5TKxR3xJ4xJSREjsmR0daXFDk_mDKs330GfthOxWQgN1r0bhB?purpose=fullsize)

* Each color = one attention cluster
* Clusters often align with **individual teeth**
* No supervision used during training

👉 The model *implicitly segments teeth* via attention

---

### 🔴 Full Jaw vs Teeth-Only Training

![Image](https://images.openai.com/static-rsc-4/7Gdeki2CTPdjHZ3OkETBHYMX7kZRk9EDTWN6mBWL-YHUYdLTz1zeJkhMVn2Tc-gISsgtbcqxoE27z36KfLEZ7W1YnxULbJbcaG__OQ0DQG6nK_UtXTMN65HLPwMpehYLAlBLwKVOJoo9j_PrTVmq56l-9BoUWP6qvi0T11y4p0btIB8X2jFavLysHETAQBHg?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/bO9EnEjUB_UelqxqI33k-FQ3mxB26dFxS0Z7T2DOj538IpdFOfL3EIKsLnLPJryGTG3kMg_eSl98Ao-xZpnmIrNrrlOJHpuZy1KvtYiqSsic9MahfADklGzDj2gVq-7Pm_WgXi40fUyDH0S0DOWqO4MrIpkDrfr9ZXCBJ4FIHwVzMpifs0KESISjo11KL6m9?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/W4h94taRXAziPIppDnRXJII4cp03lF0EfdTq9M_CLN18aQfHWqE35XHUBHKhqOzRarX_V3VJLyYnWl1bPJicPvw0oUJvK-8l8OIbQ26DyyRhBSqMQG0xWsIJELyzbsBYAehpBUNbJU6ZZUZ90lHG7eAkIftL4Du5XSpaOjnMsO_DKq05xtTeP2dGxmXf1jhK?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/f03tQV-3CPZx4UyQ6im7ccVYQ0aZsqt-HW9NAsAZlWCcRjwVVfSxIfo5-1Ugji3snYiNA1Ch7Ts4_iVlnEEE4SFK-XQ9kqkdJmi-JCGCx5YJxqHfz4kTo-vxPgXuurCI3TuPVXtaSPad5uxKvo-44LfbuQxc0ynNdqTlT0SKTIxSMJ4Mc2X0CI9ckmJYpRMb?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/BJJD2aoxSQUlv02LiJhJ5JZb0C4oDZuSVM-CoduemchNXV9KEcGL3MqgXWCJb3vKRbZdt8ByqRxe5y6NSJRQcdJgTJbsa2fv0E1eHfSB9ozpT9Y2raqoGNk3xEb-bIWJePUDqtwTvUL0ftLv-OOGgbO7_BPYCOzfDCCokT8sPBXyFU4Iy2W7tGSbJQnaw29y?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/gVQm8ZQiNiY1MIFBdCwINfzLVtMNaQTp4I2KCQXnqALS1tG3n52lhPwcx22VZU0xkLkDj9rwH2b-9fIFNfXAJPL-wS3APDH0gja5oDtdfMUtC6vuxA4t3YhFSAKP6qm-Ej-e3v15irHtqEick3Yk5iQR92A0WwqSwKMS7XbgoVV7Sg-mjpQOxJktLZa9SD23?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/JinHM1nHSC6kEhb-C4SQMWw85mYrYNWjn-0-QZHjcc1iwHJTbEWEmvtYObq35gSjOnwgEaL2zsvhYZhdM0PsOGq51guZuxB-vk30L1PnMZL1devayqXG0srVF3JDOPflBE0HfBQcBTxUEa5CmIp3ZSKtR9mJV_cw1acTC5e-euurAxeXzt6IhU8GvBzi8iNu?purpose=fullsize)

| Setting    | Observation                                 |
| ---------- | ------------------------------------------- |
| Full Jaw   | Attention spreads across teeth + background |
| Teeth Only | Clean, sharp clustering per tooth           |

👉 Removing background significantly improves structure discovery

---

## 📈 Quantitative Alignment (Attention vs Teeth)

We evaluate how well attention clusters match true tooth instances:

* **Purity ↑**
* **NMI ↑**
* **ARI ↑**
* **Entropy ↓**

Results show that:

* attention clusters are **far from random**
* they capture **meaningful anatomical structure**

---

## ⚙️ Key Features

* 🧠 **Hierarchical attention modeling** (SetVAE)
* 🦷 **3D dental geometry adaptation**
* 🔍 **Attention interpretability pipeline**
* 📊 **Unsupervised clustering evaluation**
* ☁️ Designed for **Colab / Kaggle training**

---

## 🧠 Key Insights

* Set-based generative models can **learn anatomy without labels**
* Attention provides a powerful **unsupervised segmentation signal**
* Hierarchical latent structure reflects **multi-scale geometry**
* Data preprocessing (e.g., removing background) is critical

---

## 🔬 Future Work

* integrate surface sampling
* extend to variable-size sets
* combine with segmentation supervision
* benchmark against PointNet / Point Transformer

---

## 💡 Takeaway

> **Attention-driven generative models can recover semantic structure (like teeth) directly from 3D geometry, no labels required.**

---



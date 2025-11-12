# SimDNS Dataset

SimDNS is a **simulated and GAN-augmented dataset** for encrypted DNS traffic research, focusing on **DNS-over-HTTPS (DoH)** and its privacy-enhanced variants (DoH with ESNI & DoH with ECH). It enables reproducible experiments on encrypted traffic classification, covert channel detection, and privacy-preserving communication systems.

---

## ✨ Key Features

- ✅ Realistic simulation of encrypted DNS traffic  
- ✅ Four traffic classes  
  - Standard DoH  
  - DoH with ESNI  
  - DoH with ECH  
  - HTTPS (As a comparison)  
- ✅ 34 flow features (29 side-channel features for ML tasks)  
- ✅ CTGAN-based data augmentation (~5% synthetic samples recommended)  
- ✅ Evaluated using real-world DoH dataset (CIRA-CIC-DoHBrw-2020)  
- 📈 **Best cross-dataset classification accuracy: 96.70%**

---

## 📁 Dataset Structure

```
SimDNS/
├─README.md
├─augmented dataset
│      doh with ech.csv
│      doh with esni.csv
│      doh.csv
│      https.csv
│      
└─initial dataset
        doh with ech.csv
        doh with esni.csv
        doh.csv
        https.csv
```

- **Initial dataset**: The initial dataset constructed by extracting features from realistically simulated traffic.  
- **Augmented dataset**: The enhanced dataset formed by adding 5% augmented data to the initial dataset after experimental validation. It achieves the best performance in cross-dataset training and testing experiments.

## 📦 Usage

### Clone
```bash
git clone https://github.com/YourOrg/SimDNS
cd SimDNS
```

## 🔮 Future Work

In future work, we aim to further enhance the representativeness and practical value of the SimDNS dataset. We plan to gradually incorporate real-world encrypted DNS traffic—particularly authentic DoH with ECH flows—to improve realism and broaden coverage beyond purely simulated data. Additionally, we intend to extend the dataset with typical malicious encrypted DNS traffic, such as DNS tunneling, to support research on attack detection, classification, and mitigation, thereby better addressing real-world network security monitoring needs.
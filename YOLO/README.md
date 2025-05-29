
# YOLOv8 Object Detection on Pascal VOC

Այս նախագիծը օգտագործում է **YOLOv8** մոդելը `Ultralytics` գրադարանի միջոցով՝ օբյեկտի հայտնաբերում իրականացնելու համար **Pascal VOC 2012** dataset-ի վրա։

## 📦 Նախապայմաններ

Տեղադրեք անհրաժեշտ փաթեթները՝

```bash
pip install -q ultralytics tqdm lxml matplotlib albumentations
```

---

## 📊 Ուսուցման մետրիկաներ

| Մետրիկա                   | Արժեք      |
|---------------------------|------------|
| **Best mAP@0.5**          | **0.5505** |
| Final Precision           | 0.5987     |
| Final Recall              | 0.5026     |
| Final Approx. Accuracy    | 0.5507     |
| Final Validation Box Loss | 1.1941     |
| Final Validation Cls Loss | 1.5290     |
| Final Validation DFL Loss | 1.3453     |

---

## ⚙️ Ուսուցման պարամետրեր

| Պարամետր          | Արժեք                         |
|-------------------|-------------------------------|
| Base Model        | yolov8n.pt                    |
| Image Size        | 512×512                       |
| Optimizer         | AdamW                         |
| Learning Rate     | 0.001                         |
| Final LR Factor   | 0.01                          |
| Batch Size        | 32                            |
| Epochs            | 50                            |
| Patience          | 40                            |
| Workers           | 4                             |
| Augmentation      | Ակտիվացված                   |
| Verbose           | Այո                           |
| Save Checkpoints  | Այո                           |
| Device            | GPU / CPU ըստ հասանելիության |

---

## ▶️ Ինչպես աշխատեցնել `demo.py`

`demo.py`-ն իրականացնում է օբյեկտի հայտնաբերում՝ տեսախցիկից կամ տեսանյութից։

### Օգտագործման օրինակներ

| Հրաման                                  | Նկարագրություն                          |
|----------------------------------------|-----------------------------------------|
| `python demo.py --source 0`            | Օգտագործել համակարգչի տեսախցիկը        |
| `python demo.py --source video.mp4`    | Օգտագործել տեղային տեսանյութ            |
| `python demo.py --source image.jpg`    | Օգտագործել պատկերային ֆայլ              |
| `python demo.py --source folder/`      | Վերլուծել պատկերի ֆայլերի պանակը        |


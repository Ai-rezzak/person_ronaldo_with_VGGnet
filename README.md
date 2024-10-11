# Person Ronaldo Detection with VGGNet

Bu proje, **Kaggle** üzerinde 25 epoch süresince VGGNet kullanarak eğitilmiş bir model ile insan ve Cristiano Ronaldo'nun yüzlerini tespit etmek için geliştirilmiştir. Projede iki ana dosya bulunmaktadır: biri görüntü üzerinde test yapmak için ve diğeri webcam üzerinden tespit yapmak için kullanılmaktadır.

## Proje İçeriği

### Dataset
Proje, 933 adet insan resmi ve 933 adet Cristiano Ronaldo resmi ile eğitilmiştir. Bu veriler, modelin yüzleri tanıma yeteneğini geliştirmek için kullanılmıştır.

### Eğitim
- **Model:** VGGNet
- **Epoch:** 25
- **Platform:** Kaggle

### Kullanılan Teknolojiler
- **Mediapipe:** Yüz tespiti için kullanılmıştır. Yüz tespit edildikten sonra, bu görüntü modelimize gönderilerek tespit işlemi gerçekleştirilir.
- **PyTorch:** Modelin eğitimi için kullanılmıştır.

### Kodlar
1. **cnn_ile_model_kullanma.ipynb:** 
   - Bu dosya, VGGNet modelini kullanarak yüz tespiti ve sınıflandırma işlemlerini gerçekleştiren kodları içermektedir.
  
2. **mediapipe ve model ile resim üzerinde tespit:** 
   - Bu dosya, verilen bir resim üzerinde yüz tespiti yapar. Eğer bir yüz tespit edilirse, bu yüz görüntüsü eğitilmiş model ile sınıflandırılır. 
   - **Kullanım:** 
     ```bash
      --image <resim_dosya_yolu>
     ```
   - **Parametreler:**
     - `--image`: Tespit edilmesi istenen resmin dosya yolunu belirtir. Örneğin:
       ```bash
        --image path/to/image.jpg
       ```

3. **mediapipe ve model ile webcam üzerinde tespity:** 
   - Bu dosya, webcam üzerinden gerçek zamanlı yüz tespiti yapar. Eğer bir yüz tespit edilirse, bu görüntü model ile kontrol edilerek insan mı yoksa Ronaldo mu olduğu belirlenir.
   - **Kullanım:**
     ```bash
     mediapipe ve model ile resim üzerinde tespit
     ```

## Kullanım
Gerekli kütüphanelerin yüklü olduğundan emin olun:
```bash
pip install mediapipe torch torchvision

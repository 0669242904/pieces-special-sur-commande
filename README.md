<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>طلب منتج من صفحة pièces spéciale sur commande</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-image: url('https://scontent.falg5-1.fna.fbcdn.net/v/t39.30808-6/457520434_841566134749048_8339572662356934664_n.jpg?_nc_cat=104&ccb=1-7&_nc_sid=cc71e4&_nc_ohc=TTk5c972BW0Q7kNvgF-c3k4&_nc_zt=23&_nc_ht=scontent.falg5-1.fna&_nc_gid=Alzu3GSzNdAA4qsq_OIkKz5&oh=00_AYBOxigXY5yAotmukSrYa6tps7UhUc_bFS_0_x1-uWgeAg&oe=6781ADB5');
      background-size: cover;
      background-position: center;
      margin: 0;
      padding: 20px;
      direction: rtl;
      text-align: right;
    }
    .product-page {
      max-width: 1200px;
      margin: 0 auto;
      background: rgba(255, 255, 255, 0.9);
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
    .product-title {
      text-align: center;
      font-size: 24px;
      margin-bottom: 20px;
      color: #333;
    }
    .product-details {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }
    .product-image {
      width: 48%;
      margin-bottom: 20px;
    }
    .product-image img {
      width: 100%;
      border-radius: 8px;
    }
    .product-info {
      width: 48%;
    }
    .form-group {
      margin-bottom: 15px;
    }
    .form-group label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }
    .form-group input, .form-group select {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
      background-color: #fff;
    }
    .form-group input:focus, .form-group select:focus {
      outline: none;
      border-color: #007bff;
    }
    .btn {
      display: block;
      width: 100%;
      padding: 10px;
      background: #007bff;
      color: #fff;
      border: none;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
    }
    .btn:hover {
      background: #0056b3;
    }
    .whatsapp-btn {
      margin-top: 20px;
      display: block;
      text-align: center;
      background-color: #25d366;
      color: white;
      padding: 12px 20px;
      font-size: 16px;
      border-radius: 5px;
      text-decoration: none;
    }
    .whatsapp-btn:hover {
      background-color: #128c7e;
    }
  </style>
</head>
<body>
  <div class="product-page">
    <h2 class="product-title">طلب منتج من صفحة pièces spéciale sur commande</h2>
    <div class="product-details">
      <div class="product-image">
        <img id="product-image" src="https://link_to_default_image.jpg" alt="منتج" />
      </div>
      <div class="product-info">
        <h3>اختار المنتج</h3>

        <form id="checkout-form">
          <div class="form-group">
            <label for="full-name">الاسم الكامل</label>
            <input type="text" id="full-name" name="full-name" placeholder="مثال: أحمد محمد" required>
          </div>
          <div class="form-group">
            <label for="phone">رقم الهاتف</label>
            <input type="tel" id="phone" name="phone" placeholder="مثال: 0770123456" required>
          </div>
          <div class="form-group">
            <label for="address">العنوان</label>
            <input type="text" id="address" name="address" placeholder="مثال: شارع التحرير، الجزائر العاصمة" required>
          </div>
          <div class="form-group">
            <label for="state">الولاية</label>
            <select id="state" name="state" required>
              <option value="">اختر الولاية</option>
              <option value="algiers">الجزائر</option>
              <option value="oran">وهران</option>
              <option value="constantine">قسنطينة</option>
              <option value="annaba">عنابة</option>
              <!-- أضف المزيد من الخيارات إذا لزم الأمر -->
            </select>
          </div>
          <div class="form-group">
            <label for="delivery-type">نوع التوصيل</label>
            <select id="delivery-type" name="delivery-type" required>
              <option value="">اختر نوع التوصيل</option>
              <option value="home">إلى البيت</option>
              <option value="office">إلى المكتب</option>
            </select>
          </div>
          <div class="form-group">
            <label for="delivery-price">سعر التوصيل</label>
            <input type="text" id="delivery-price" name="delivery-price" placeholder="سيتم حسابه تلقائيًا" readonly>
          </div>

          <div class="form-group">
            <label for="product">المنتج</label>
            <select id="product" name="product" required onchange="updateProductImage()">
              <option value="exol_0w30">Exol 0W30</option>
              <option value="exol_5w40">Exol 5W40 FS</option>
              <option value="exol_10w40_gris">Exol 10W40 Bidon Gris</option>
              <option value="exol_10w40_ssx">Exol 10W40 SSX</option>
            </select>
          </div>

          <button type="submit" class="btn">إرسال الطلب</button>
        </form>
        
        <a href="https://wa.me/0669242904" class="whatsapp-btn" target="_blank">استفسار عبر واتساب</a>
      </div>
    </div>
  </div>

  <script>
    // دالة لتحديث صورة المنتج بناءً على الاختيار
    function updateProductImage() {
      var product = document.getElementById("product").value;
      var image = document.getElementById("product-image");

      // إضافة صور للمنتجات بناءً على الاختيار
      if (product === "exol_0w30") {
        image.src = "https://link_to_exol_0w30_image.jpg"; // صورة المنتج Exol 0W30
      } else if (product === "exol_5w40") {
        image.src = "https://link_to_exol_5w40_image.jpg"; // صورة المنتج Exol 5W40
      } else if (product === "exol_10w40_gris") {
        image.src = "https://link_to_exol_10w40_gris_image.jpg"; // صورة المنتج Exol 10W40 Gris
      } else if (product === "exol_10w40_ssx") {
        image.src = "https://link_to_exol_10w40_ssx_image.jpg"; // صورة المنتج Exol 10W40 SSX
      }
    }

    // إضافة وظيفة لحساب سعر التوصيل
    document.getElementById("checkout-form").addEventListener("submit", function(event) {
      event.preventDefault();
      const state = document.getElementById("state").value;
      const deliveryType = document.getElementById("delivery-type").value;

      if (!state || !deliveryType) {
        alert("يرجى تحديد الولاية ونوع التوصيل");
        return;
      }

      fetch(`https://api.example.com/get-delivery-price?state=${state}&delivery_type=${deliveryType}`)
        .then(response => response.json())
        .then(data => {
          if (data && data.delivery_price) {
            document.getElementById("delivery-price").value = `${data.delivery_price} دج`;
          } else {
            alert("لم يتم العثور على سعر التوصيل.");
          }
        })
        .catch(error => {
          console.error("حدث خطأ أثناء جلب سعر التوصيل:", error);
          alert("حدث خطأ. يرجى المحاولة لاحقًا.");
        });
    });
  </script>
</body>
</html>

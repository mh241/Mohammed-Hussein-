# Mohammed-Hussein-# 1. الدخول لمجلد المشروع
cd ~/sina-falcon

# 2. إنشاء ملف البيئة (environment.yml)
cat << 'EOF' > environment.yml
name: sina-falcon-env
channels:
  - conda-forge
  - defaults
dependencies:
  - python=3.10
  - pandas
  - pip
  - pip:
    - google-cloud-firestore
    - firebase-admin
EOF

# 3. رفع الملف للمستودع (عشان السيرفر يشوفه)
git add environment.yml
git commit -m "إضافة ملف البيئة لتصحيح خطأ بناء لينكس"
git push origin main

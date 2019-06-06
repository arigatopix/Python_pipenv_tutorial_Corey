# PIPENV
ช่วยในการจัดการ environment กับ package
Pipfile บอก version 
Pipfile.lock เป็นตัวกำหนด version ที่ใช้งานจริง (จะเปลี่ยนไปตาม Pipfile)

#### INSTALL
`pip install pipenv`

#### INSTALL PACKAGE
`pipenv install requests`

#### activate
`pipenv shell`

#### deactivate
`exit`

#### install requirements.txt
`pipenv install -r ../folder/requirements.txt`

#### create requirements.txt ให้กับคนใช้ pip (เหมือน pip freeze)
`pipenv lock -r`

#### วิธี install package เฉพาะ dev-dependencies
`pipenv install pytest --dev`

#### uninstall package
`pipenv uninstall requests`

#### ถ้าอยากเปลี่ยน version python 
เปลี่ยนที่ Pipfile เป็น version ที่ต้องการ (ในที่นี่้เปลี่ยนจาก python 3.7 เป็น python 3.6) จากนั้น
`pipenv --python 3.6`

#### check package version
`pipenv check`

#### update package ไปเปลี่ยนทีื Pipfile แล้วพิมพ์
`pipenv install`

#### remove entire virtual environment
`pipenv --rm`

#### install package จาก Pipfile
`pipenv install`

#### หา path ของ virtual env
`pipenv --venv`

#### วิธีดูว่า package ไหนอยู่ใน lib ของใคร
`pipenv graph`

#### dev to production พวก version ที่ใช้งานจะบรรจุใน Pipfile.lock ดังนั้นต้อง update .lock ก่อน
`pipenv lock`

#### install package ใน production 
`pipenv install --ignore-pipfile`

### ใช้ SECRET_KEY หรือ DATABASE อันเดียว กับหลายๆ project โดยใช้ .env แต่ไม่ต้อง commit ใน github

##### create .env เพื่อเก็บข้อมูล
`touch .env`

#### วิธีใช้งาน ปกติ python จะ load .env มาใช้งานในโปรเจคให้อัตโนมัติ
`pipenv run python`

#### ลองเรียกดู
`import os`
`os.environ['SECRET_KEY']`
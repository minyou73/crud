# CRUD

## 프로젝트 구조 작성

1. 프젝트 폴더 생성
2. 프젝트 폴더를 vscode로 열기
    - `.gitignore`, `README.md` 만들기
3. django 프로젝트 생성
```
django-admin startproject <pjt-name>. 
```
4. 가상환경 설정
```
python -m venv venv
```
  - 파이썬을 통해 venv라이브러리 사용하겠다. 인자는 venv
  - git으로 관리 되지 않음

5. 가상환경 활성화 
    -(venv)가 터미널에 출력 되었는지 확인
```
source venv/Scripts/activate
source venv/bin/activate

```
6. 가상환경에 django 설치
```
pip install django
```

7. 서버 실행 확인
```
python manage.py runserver
```

8. 앱 생성
```
django-admin startapp <app-name>
```

9. 앱 등록 =>  `settings.py`
```python
INSTALLED_APPS= [
    ...
    '<appname>',
]
```

10. `urls.py` > `views.py` > `template/*.html` 순서로 코드 작성



## Model
1. 모델 정의(  `models.py`)
    - 모델의 이름은 기본적으로 단수 형태

```python
class Post(models.Model):
    title = models.CharField(max_length = 100)
    content = models.TextFild()
```
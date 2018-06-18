# IBVP layout
#####참고사이트
 - [Bootstrapk](http://bootstrapk.com/css/)
 - [AdminLTE](https://adminlte.io/themes/AdminLTE/index2.html)
***
## 1. grid
#### 1.1. 기본 클래스
1. ```.row```로 감싸줘야함
2. ```.col-*```은 총 12 가 되는 하나의 컬럼 세트

```
<div class="row">
    <div class="col-md-4">.col-md-4</div>
    <div class="col-md-4">.col-md-4</div>
    <div class="col-md-4">.col-md-4</div>
</div>

<div class="row">
    <div class="col-md-6">.col-md-6</div>
    <div class="col-md-6">.col-md-6</div>
</div>
```
####1.2. 컬럼 중첩하기
- 존재하는 ```.col-*``` 컬럼 내에 새로운 ```.row``` 와 ```.col-*``` 컬럼 세트를 추가
- 중첩된 행은 합쳐서 12 가 되는 하나의 컬럼 세트를 포함

```
<div class="row">
    <div class="col-md-9">
        <div class="row">
            <div class="col-xs-8 col-md-6"></div>
            <div class="col-xs-4 col-md-6"></div>
        </div>
    </div>
    <div class="col-md-3">
        <div class="row">
            <div class="col-xs-8 col-md-6"></div>
            <div class="col-xs-4 col-md-6"></div>
        </div>
    </div>
</div>
```
***
## 2. table
#### 2.1. ```<table>``` 기본 클래스
- ```.table```

#### 2.2. ```<table>``` 에 추가 가능한 css
- ```.table-bordered``` (all라인) / ```.table-striped``` (짝수라인 색을 넣음)
- ```.table-condensed``` (tr 위아래 간격이 좁음)
- ```.table-hover``` (hover시 tr라인에 색상)
- ```.text-center```

```
<table class="table">
    <colgroup>
        <!-- 테이블 td 갯수만큼 col 생성 -->
        <col style="width: ;" />
        <col style="width: ;" />
    </colgroup>
    <thead>
        <tr>
            <th scope="col"></th>
            <th scope="col"></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td scope="row"></td>
            <td></td>
        </tr>
    </tbody>
</table>
```

#### 2.3. thead 고정 테이블 
1. ```.table-area```, ```.tb-scroll``` 으로 ```<table>```을 감싸준다.
2. ```<table>``` >  ```<th>``` > ```div.fixed```을 추가한다.

```
<div class="table-area">
    <div class="tb-scroll">
        <div class="tb-fixed-head"></div>
        <table>...</table>
    </div>
</div>
```

> - 2.의 ```div.fixed``` 추가시 style width값은 해당 ```<col>```의 값과 같게한다.

```
    <table class="table table-bordered text-center table-hover">
        <colgroup>
            <col style="width: 5%;">
            <col style="width: 80%;">
            <col style="width: 15%;">
        </colgroup>
        <thead>
            <tr>
                <th><div class="fixed" style="width: 5%;">...</div></th>
                <th><div class="fixed" style="width: 80%;">...</div></th>
                <th><div class="fixed" style="width: 15%;">...</div></th>
            </tr>
        </thead>
    </table>
```

****
## 3. form
### 3.1. 폼 관련 레이아웃 css
#### 3.1.1. block form (기본)

```
<form>
    <div class="form-group">
        <label for="email1">이메일 주소</label>
        <input type="email" class="form-control" id="email1" placeholder="이메일을 입력하세요">
    </div>
</form>
```

#### 3.1.2. inline form (한 라인에 input 한 줄로)
>   ```<form>``` 아닌 ```<div>```도 class 추가 가능.

```
<form class="form-inline">
    <div class="form-group">
        <label for="name2">Name</label>
        <input type="text" class="form-control" id="name2" placeholder="Jane Doe">
    </div>
    <div class="form-group">
        <label for="email2">Email</label>
        <input type="email" class="form-control" id="email2" placeholder="jane.doe@example.com">
    </div>
    <button type="submit" class="btn btn-default">Send invitation</button>
</form>
```

#### 3.1.3. horizontal form (수평)
>   ```<form>``` 아닌 ```<div>```도 class 추가 가능.

```
<form class="form-horizontal">
    <div class="form-group">
        <label for="email3" class="col-sm-2 control-label">Email</label>
        <div class="col-sm-10">
            <input type="email" class="form-control" id="email3" placeholder="Email">
        </div>
    </div>
</form>
```

### 3.2. 지원되는 콘트롤들
> 폼 레이아웃 예제에서 지원되는 표준 폼콘트롤 예제들.
#### 3.2.1. inputs
- ```<input>``` ,```<select>```, ```<textarea>``` 에 ```.form-control``` 적용.

```
<input type="text" class="form-control" placeholder="Text input">

<select class="form-control">
    <option>1</option>
    <option>2</option>
</select>

<textarea class="form-control" rows="3"></textarea>
```

#### 3.2.2. 체크박스와 라디오
- 기본   (block)  : ```<div>```에  ```.radio``` 또는 ```.checkbox``` 적용.
- 인라인 (inline) : ```<div>```에  ```.radio-inline``` 또는 ```.checkbox-inline``` 적용.
- 사용자들이 라벨에 마우스를 올렸을 때 "허락되지 않은" 커서를 표시하려면, ```disabled``` 추가.

```
<div class="checkbox">
    <label>
        <input type="checkbox" value="">
        checkbox
    </label>
</div>

<div class="radio-inline">
    <label>
        <input type="radio" name="optionsRadios" id="optionsRadios1" value="option1" checked>
        radio inline
    </label>
</div>   

<div class="checkbox disabled">
    <label>
        <input type="checkbox" value="" disabled>
        checkbox disabled
    </label>
</div>

```

#### 3.2.3. 입력 그룹
##### 기본
****
## 4. button
### 4.1. ```<button>``` 에 추가 가능한 css
#### 4.1.1. 기본 클래스
- ```.btn```

#### 4.1.2. 추가 클래스
- ```.btn-default``` / ```.btn-primary``` / ```.btn-success``` / ```.btn-info``` / ```.btn-danger``` / ```.btn-warning``` (컬러)
- ```.btn-lg``` / ```.btn-sm``` / ```.btn-xs``` (사이즈)
- ```.btn-group``` / ```.btn-group-vertical``` (그룹으로 만들어준다. 붙어있음)
- ```.btn-flat``` (각진버튼)
- ```.disabled```

```
<button type="button" class="btn btn-default">button</button>
```

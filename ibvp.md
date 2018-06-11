# IBVP layout

## table
### ````<table>```` 에 추가 가능한 css

> #### 기본 클래스
>   - **table**

> #### 추가 클래스
>   - **table-bordered** (all라인) / **table-striped** (2n 색바뀜)
>   - **table-condensed** (tr 위아래 간격이 좁음)
>   - **table-hover** (hover시 tr라인에 색상)
>   - **text-center**

````
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
````

> #### thead 고정 테이블 
>   - ````<table>````을 감싸줘야하는 기본 셋팅
>   ````
>   <div class="table-area">
>       <div class="tb-scroll">
>           <div class="tb-fixed-head"></div>
>           <table>...</table>
>       </div>
>   </div>
>   ````
>   - ````<table>````에 적용하여야 하는 class 
>   ````
>   <table class="table table-bordered text-center table-hover">
>       <colgroup>
>           <col style="width: 5%;">
>           <col style="width: 80%;">
>           <col style="width: 15%;">
>       </colgroup>
>       <thead>
>           <tr>
>               <th><div class="fixed" style="width: 5%;">...</div></th>
>               <th><div class="fixed" style="width: 80%;">...</div></th>
>               <th><div class="fixed" style="width: 15%;">...</div></th>
>           </tr>
>       </thead>
>   </table>
>   ````

## form
### form 관련 layout css

> #### 1.block form (기본)

````
<form>
    <div class="form-group">
        <label for="exampleInputEmail1">이메일 주소</label>
        <input type="email" class="form-control" id="exampleInputEmail1" placeholder="이메일을 입력하세요">
    </div>
</form>
````

> #### 2.inline form (한 라인에 input 한 줄로)
>   - form 아닌 div도 class 추가 가능

````
<form class="form-inline">
    <div class="form-group">
        <label for="exampleInputName2">Name</label>
        <input type="text" class="form-control" id="exampleInputName2" placeholder="Jane Doe">
    </div>
    <div class="form-group">
        <label for="exampleInputEmail2">Email</label>
        <input type="email" class="form-control" id="exampleInputEmail2" placeholder="jane.doe@example.com">
    </div>
    <button type="submit" class="btn btn-default">Send invitation</button>
</form>
````

> #### 3. horizontal form (수평)
>   - form 아닌 div도 class 추가 가능

````
<form class="form-horizontal">
    <div class="form-group">
        <label for="inputEmail3" class="col-sm-2 control-label">Email</label>
        <div class="col-sm-10">
            <input type="email" class="form-control" id="inputEmail3" placeholder="Email">
        </div>
    </div>
</form>
````

### ````<input>```` 에 추가 가능한 css

> #### 기본 클래스
>   - **form-control**
>   ````
>   <input type="text" class="form-control" placeholder="Text input">
>   <textarea class="form-control" rows="3"></textarea>
>   ````

> #### 체크박스와 라디오
>   ##### 기본 (block)
>       - ````.radio````, ````.checkbox````
>       - 사용자들이 라벨에 마우스를 올렸을 때 "허락되지 않은" 커서를 표시하려면, ````disabled```` 추가
>       ````
>       <div class="checkbox">
          <label>
            <input type="checkbox" value="">
            Option one is this and that&mdash;be sure to include why it's great
          </label>
        </div>
        <div class="checkbox disabled">
          <label>
            <input type="checkbox" value="" disabled>
            Option two is disabled
          </label>
        </div>

        <div class="radio">
          <label>
            <input type="radio" name="optionsRadios" id="optionsRadios1" value="option1" checked>
            Option one is this and that&mdash;be sure to include why it's great
          </label>
        </div>        
        <div class="radio disabled">
          <label>
            <input type="radio" name="optionsRadios" id="optionsRadios3" value="option3" disabled>
            Option three is disabled
          </label>
        </div>
>       ````

## button
### ````<button>```` 에 추가 가능한 css

> #### 기본 클래스
>   - **btn**

> #### 추가 클래스
>   - **btn-default** / **btn-primary** / **btn-success** / **btn-info** / **btn-danger** / **btn-warning** (컬러)
>   - **btn-lg** / **btn-sm** / **btn-xs** (사이즈)
>   - **btn-group** / **btn-group-vertical** (그룹으로 만들어준다. 붙어있음)
>   - **btn-flat** (각진버튼)
>   - **disabled**

````
<button type="button" class="btn btn-default">button</button>
````

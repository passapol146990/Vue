<template>
  <div>
    <!-- รวมแทบเมนูบน -->
    <div>
      <!-- เข้าสู่ระบบ -->
      <div class="container text-center mt-5">
        <div class="text-center">
          <p class="alert alert-info border border-dark my-2">
            กดเข้าสู่ระบบเพื่อไปยังหน้าเช็คชื่อนักศึกษาวิชาทหารของท่าน
          </p>
          <button
            data-bs-target="#showform"
            data-bs-toggle="modal"
            aria-labelledby="staticBackdropLable"
            aria-hidden="true"
            class="btn btn-primary btn-lg"
            style="border-radius: 10px"
          >
            เข้าสู่ระบบ
          </button>
        </div>
        <!-- formpopup -->
        <div
          class="modal fade"
          id="showform"
          data-bs-keyboard="false"
          tabindex="-1"
          aria-labelledby="staticBackdropLable"
          aria-hidden="true"
        >
          <div class="modal-dialog">
            <div class="modal-content">
              <div class="modal-header">
                <h3>เข้าสู่ระบบ</h3>
                <button
                  type="button"
                  class="btn-close"
                  data-bs-dismiss="modal"
                  aria-label="Close"
                ></button>
              </div>
              <div class="modal-body">
                <!-- loginForm -->
                <form id="loginForm">
                  <div class="form-group text-start">
                    <label class="control-label"
                      >Login:Password is in a line group</label
                    >
                    <input
                      name="password1"
                      placeholder="Password1"
                      type="password"
                      class="my-2 form-control is-valid"
                    />
                  </div>
                  <div class="form-group text-start">
                    <input
                      name="password2"
                      placeholder="Password2"
                      type="password"
                      class="my-2 form-control is-valid"
                    />
                  </div>

                  <div class="form-group text-end">
                    <button class="btn btn-success">เข้าสู่ระบบ</button>
                    <hr />
                    <div class="col">
                      <label id="title">ใส่รหัสผ่าน</label>
                      <label id="ToForm"></label>
                    </div>
                  </div>
                </form>
              </div>
              <div class="modal-footer">
                <p class="text-danger">
                  !เฉพาะบุคคลที่ได้รับหน้าที่ในการเช็คชื่อเท่านั้น
                  หากเข้าไม่ได้กรุณาติดต่อผู้ดูแลระบบ!
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- ดูชื่อตัวเอง -->
      <div class="container text-center my-4 mt-5">
        <p class="alert alert-info border border-dark my-2">
          เช็คหมู่ตัวเอง ตรวจสอบการมาเรียน - ขาดเรียน
        </p>
        <a
          href="#checkname"
          class="btn btn-primary"
          data-bs-target="#checkname"
          data-bs-toggle="modal"
          >ดูชื่อตัวเอง มา-ขาด</a
        >
      </div>
      <div
        class="modal fade"
        id="checkname"
        data-bs-keyboard="false"
        tabindex="-1"
        aria-labelledby="staticBackdropLable"
        aria-hidden="true"
      >
        <div class="modal-dialog">
          <div class="modal-content">
            <div class="modal-header">
              <h3>เช็คหมู่ตัวเอง ตรวจสอบการมาเรียน - ขาดเรียน</h3>
              <button
                class="btn-close"
                data-bs-dismiss="modal"
                aria-label="Close"
              ></button>
            </div>
            <div class="modal-body">
              <div class="container">
                <ul class="border border-2">
                  <li>ตรวจสอบหมู่ตัวเอง</li>
                  <a
                    target="_blank"
                    href="https://drive.google.com/drive/folders/1Rots6JEmHvThZ0c9fOfsNHcfKpnrYysD?usp=sharing"
                    class="btn btn-warning form-control mb-3"
                    >ตรวจสอบหมู่ตัวเอง</a
                  >
                </ul>
                <ul class="border border-2">
                  <li>ตรวจสอบ มา-ขาด</li>
                  <a
                    target="_blank"
                    href="https://drive.google.com/drive/folders/1iYcP3NQLBunP259et9s7TQpAAkPUbJAe?usp=sharing"
                    class="btn btn-success form-control mb-3"
                    >เช็คชื่อมา-ขาด</a
                  >
                </ul>
              </div>
            </div>
            <div class="modal-footer"></div>
          </div>
        </div>
      </div>
    </div>
    <hr />

    <!-- ระบบเช็คชื่อ -->
    <div
      class="modal fade"
      id="EditForm"
      data-bs-keyboard="false"
      tabindex="-1"
      aria-labelledby="staticBackdropLable"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h3>เลือกหมู่ที่ตัวท่านรับผิดชอบ</h3>
          </div>
          <div class="modal-body">
            <div class="card mb-3">
              <div class="p-3">
                <h4>เช็คชื่อเช้า</h4>
                <a
                  class="form-control btn btn-primary"
                  mt-2
                  data-bs-target="#EditForm1"
                  data-bs-toggle="modal"
                  aria-labelledby="statocBackdropLevle"
                  aria-hidden="true"
                  >เช็คชื่อเช้า</a
                >
              </div>
            </div>
            <div class="card">
              <div class="p-3">
                <h4>เช็คชื่อเย็น</h4>
                <a
                  class="form-control btn btn-danger mt-2"
                  data-bs-target="#EditForm2"
                  data-bs-toggle="modal"
                  aria-labelledby="staticBackdropLable"
                  aria-hidden="true"
                  >เช็คชื่อเย็น</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- ระบบเช็คชื่อเช้า-->
    <div
      class="modal fade"
      id="EditForm1"
      data-bs-keyboard="false"
      tabindex="-1"
      aria-labelledby="staticBackdropLable"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h3>เลือกหมู่ที่ตัวท่านรับผิดชอบ</h3>
            <button
              class="btn btn-white"
              type="button"
              data-bs-target="#EditForm"
              data-bs-toggle="modal"
              aria-labelledby="staticBackdropLable"
              aria-hidden="true"
            >
              =กลับ
            </button>
          </div>
          <div class="modal-body">
            <h1 class="alert alert-success">เช็คชื่อตอน เช้า</h1>
            <h1 class="alert alert-info border-dark">
              นักศึกษาวิชาทหาร โรงเรียนกมลาไสย
            </h1>
            <div class="row my-5">
              <div class="card">
                <!--ปี 1-->
                <h2 class="alert alert-secondary my-3">
                  เช็คชื่อตามหมู่ รด.ปี 1 โรงเรียนกมลาไสย
                </h2>
                <div class="mb-3">
                  <h4 class="alert alert-success">เช้า</h4>
                  <tr>
                    <a
                      href="https://docs.google.com/spreadsheets/d/10IYKzeYIQJUXlRUZYSUlbz-MelBkYilCSlQMaw9QsVY/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1vG8ONBYW5WewDv_qXOLp75GxRj4VEJf4tZvCKgTmH8I/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่2</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1IL1yszNk8qvaOa324esprLRIeRNhl-y1iN0boaQVK08/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่3</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1Shbv5iOxQU2-S11Dzflj_vTlGO6kgKAHZiqps61H0MM/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่4</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1zU9SLDzC3DtgcGJ2XA0r-oOX7hFmLBccoeHHKVp4d6E/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่5</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/12_Vze6yPHxdCM5l3t5lYSpYF1zCSwxLH24Ip5u4OI4I/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1หญิง</a
                    >
                  </tr>
                </div>
              </div>
            </div>
            <div class="row my-5">
              <div class="card">
                <!--ปี 2-->
                <h2 class="alert alert-secondary my-3">
                  เช็คชื่อตามหมู่ รด.ปี 2 โรงเรียนกมลาไสย
                </h2>
                <div class="mb-3">
                  <h4 class="alert alert-success">เช้า</h4>
                  <tr>
                    <a
                      href="https://docs.google.com/spreadsheets/d/1ngVRdnULpWrBYV69srYEy74P-xRcp9-NatBLzPHy8oI/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1ZRHFU8nrTtZXVfFquf80eWvLooZyetRxx5kvmK6hTM0/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่2</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1Is-Z6nGGp2NzG4J_ek8VfkQHeQMM0Bkis0nMhygQPZU/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่3</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1cSDY7cNT5Kvys9mmzGsC8q-VMkygx6UZQmBXl5jXLXw/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่4</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1FE5qCRmCGXscw3Ju67J8mhojbAtWFFNFX3EuM4FZo-U/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่5</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/14q4nULW1ygjbRUNtmozrvaMYaWvpbYAIvFPSdF8myyo/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1หญิง</a
                    >
                  </tr>
                </div>
              </div>
            </div>
            <div class="row my-5">
              <div class="card">
                <!--ปี 3-->
                <h2 class="alert alert-secondary my-3">
                  เช็คชื่อตามหมู่ รด.ปี 3 โรงเรียนกมลาไสย
                </h2>
                <div class="mb-3">
                  <h4 class="alert alert-success">เช้า</h4>
                  <tr>
                    <a
                      href="https://docs.google.com/spreadsheets/d/1EF5Bk7eK0taJ1gfL5pPRRKKIpAUpVJ3YLjApb1IIYx4/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1DsoQTBlsA4fMnl5dMGFh1Zdj9loFsHh5Kbsa8aqILhY/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่2</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/18KcOwtbw-suI0Z_ISxx5heac8Q306rgc9KlxKZCJ4s4/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่3</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1cjGhFkx3oVVP9xeY1_TzOo2f1FoAsVNCSDrMjnPQZos/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่4</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1mZHqmll4Secj1QFgMvT74ozow51v1NiluWzNmu_c6gM/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่5</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1QswcRsX10WLmYPNfpBS9U30me55SrB7jYXHAu82l95s/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1หญิง</a
                    >
                  </tr>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- ระบบเช็คชื่อเย็น -->
    <div
      class="modal fade"
      id="EditForm2"
      data-bs-keyboard="false"
      tabindex="-1"
      aria-labelledby="staticBackdropLable"
      aria-hidden="true"
    >
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h3>เลือกหมู่ที่ตัวท่านรับผิดชอบ</h3>
            <button
              class="btn btn-white"
              data-bs-target="#EditForm"
              data-bs-toggle="modal"
              aria-labelledby="staticBackdropLable"
              aria-hidden="true"
            >
              กลับ
            </button>
          </div>
          <div class="modal-body">
            <h1 class="alert alert-success">เช็คชื่อตอน เย็น</h1>
            <h1 class="alert alert-info border-dark">
              นักศึกษาวิชาทหาร โรงเรียนกมลาไสย
            </h1>
            <div class="row my-5">
              <div class="card">
                <!--ปี 1-->
                <h2 class="alert alert-secondary my-3">
                  เช็คชื่อตามหมู่ รด.ปี 1 โรงเรียนกมลาไสย
                </h2>
                <div class="mb-3">
                  <h4 class="alert alert-success">เย็น</h4>
                  <tr>
                    <a
                      href="https://docs.google.com/spreadsheets/d/1KIOMaB8nqieYiRCYPpZ_nQrvmMu9SIafe9OjPZ7neB4/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1KLG94ygSuI-9bDFc8dy6nMnIxw1ivdxPvN_4jZVGusM/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่2</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1fQ1APJddaI6fYCmgmy_VQK_QMuzJ3ZQU__7A4taPyEA/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่3</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1LsXwru_SuEi1vN0z5ZzeEzn9l7X86c3btuubLPHXbPY/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่4</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1E3ku6yWjlfuX3cCW86sHC6RAioX7oAf-lmM4Xr8YA4U/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่5</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1xF0A8UOKAyx3Hjhhyn-dTkXpxfEFN3bWGw-mMVZpqDE/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1หญิง</a
                    >
                  </tr>
                </div>
              </div>
            </div>
            <div class="row my-5">
              <div class="card">
                <!--ปี 2-->
                <h2 class="alert alert-secondary my-3">
                  เช็คชื่อตามหมู่ รด.ปี 2 โรงเรียนกมลาไสย
                </h2>
                <div class="mb-3">
                  <h4 class="alert alert-success">เย็น</h4>
                  <tr>
                    <a
                      href="https://docs.google.com/spreadsheets/d/1z1qFXYD4xEJG5d8TR_IAyYL35Oec44GWBwdx45KtSKs/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1ED6c7O2H0bfDmCWfqpEcX7t3AXQa4R8duvcMBwVva9c/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่2</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1YASMOuRze7NK3RticWdVWt2nK46G8GdE2WppcY-n37U/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่3</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1-E80Skcpisk1CL45d0IaWfvf-_zsasl-xWlTnQup0AM/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่4</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1bpgxvcJIAIkaFbSynLhL35HIoFuHtLTUhzDuFTniteM/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่5</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1OcD8VsPccYGsDtKlo8DNBsn7vSajv0dtUmwOboat-BU/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1หญิง</a
                    >
                  </tr>
                </div>
              </div>
            </div>
            <div class="row my-5">
              <div class="card">
                <!--ปี 3-->
                <h2 class="alert alert-secondary my-3">
                  เช็คชื่อตามหมู่ รด.ปี 3 โรงเรียนกมลาไสย
                </h2>
                <div class="mb-3">
                  <h4 class="alert alert-success">เย็น</h4>
                  <tr>
                    <a
                      href="https://docs.google.com/spreadsheets/d/1TuyWblMTOQsPiZW-uGlnqzgbsQnf127J3Juw4gbJoVk/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1_VjSNOw0tnUMQpWeoRhjgy8Cvg3DSXjs29wCYOw4OaY/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่2</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/16w83gGdvf8o87X-mOx_ERG8YF18wKvpVCk6typAxdIA/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่3</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1XNRCwdeflsw64zlJA4DJjS_Gpxh4dOzhzaxCXOT7P0c/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่4</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1gYig7rbAILEkTF9wK38eOO8bEHAPhNLj2IBmWDgE0YU/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่5</a
                    >
                    <a
                      href="https://docs.google.com/spreadsheets/d/1BDkFuVMknWhyM2j7En1xIg9rztnLKmbcHgCcPbNvzzs/edit?usp=sharing"
                      class="btn btn-outline-primary"
                      >หมู่1หญิง</a
                    >
                  </tr>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
body {
  color: #fff;
}
</style>

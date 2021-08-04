<template>
  <div class="row">
    <div class="col-lg-12">
      <div class="card card-custom card-gutter">

        <div class="card-header border-0 py-5">
          <h3 class="card-title align-items-start flex-column">
            {{ $t('Subscribers') }}
          </h3>
        </div>
        <!--begin: card-body-->
        <div class="card-body pt-0 pb-3">
          <div class="table-responsive">

            <div class="d-flex align-items-center pb-5 py-5">
              <form>
                <div class="input-group input-group-sm input-group-solid">
                  <input type="text" class="form-control" placeholder="Name">
                  <input type="text" class="form-control" placeholder="E-mail">
                  <input type="text" class="form-control" placeholder="Phone">
                  <input type="text" class="form-control" placeholder="Card">
                </div>
              </form>
            </div>

            <table class="table table-head-custom table-head-bg table-borderless table-vertical-center">
              <thead>
                <tr class="text-uppercase">
                  <TableTh v-for="th in fields" :width="th.width" :className="th.className">{{th.name}}</TableTh>
                </tr>
              </thead>
              <tbody>
                <tr v-for="trItems in subscribers">
                  <td v-for="td in trItems">
                    <span class="text-dark-75 font-weight-bolder d-block font-size-lg">{{td}}</span>
                  </td>
                </tr>

              </tbody>
            </table>
          </div>
        </div>
        <!--end: card-body-->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Table",
  props: {
    title: { type: String }
  },
  data() {
    return {
      fields: [
        { name: "ID", width: 30, className: true },
        { name: "Count", width: 30, className: "" },
        { name: "Group", width: 100, className: "" },
        { name: "Name", width: 100, className: "" },
        { name: "Data", width: 100, className: "" },
        { name: "E-mail", width: 100, className: "" },
        { name: "Phone", width: 100, className: "" },
        { name: "Expires", width: 100, className: "" },
        { name: "Card", width: 100, className: "" },
        { name: "Actions", width: 100, className: "" },
      ],
      subscribers: [
        [
          1,
          3,
          "KL-90",
          "Tony",
          "2021-08-20",
          "tony@test.com",
          "+1984402223",
          "2021-09-20",
          "567664..4455"
        ],
        [
          2,
          4,
          "KL-91",
          "Tony3",
          "2021-08-20",
          "tony@test.com",
          "+1984402223",
          "2021-09-20",
          "567664..4455"
        ],
      ],
      tableThHTML: ""
    }
  },
  created() {
    //this.getTableHeader()
  }, // end created
  methods: {

    getTableHeader () {
      //<th style="min-width: 30px" class="pl-7">ID</th>
      let headerFields = this.fields;
      for (let i in headerFields) {
        if (headerFields.hasOwnProperty(i)) {
          let th = document.createElement("th");

          if (headerFields[i].className.length > 1) {
            th.setAttribute("class", headerFields[i].className)
          }
          if (headerFields[i].width) {
            th.style.cssText = 'min-width:' + headerFields[i].width + 'px';
          }
          if (headerFields[i].name) {
            th.innerText = headerFields[i].name;
          }
          console.log(th)
          this.tableThHTML += th;
        }
      }
    }

  } // end methods

}
</script>

<style scoped>

</style>

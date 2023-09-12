<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br />
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener"
        >vue-cli documentation</a
      >.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li>
        <a
          href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel"
          target="_blank"
          rel="noopener"
          >babel</a
        >
      </li>
      <li>
        <a
          href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint"
          target="_blank"
          rel="noopener"
          >eslint</a
        >
      </li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li>
        <a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a>
      </li>
      <li>
        <a href="https://forum.vuejs.org" target="_blank" rel="noopener"
          >Forum</a
        >
      </li>
      <li>
        <a href="https://chat.vuejs.org" target="_blank" rel="noopener"
          >Community Chat</a
        >
      </li>
      <li>
        <a href="https://twitter.com/vuejs" target="_blank" rel="noopener"
          >Twitter</a
        >
      </li>
      <li>
        <a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a>
      </li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li>
        <a href="https://router.vuejs.org" target="_blank" rel="noopener"
          >vue-router</a
        >
      </li>
      <li>
        <a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a>
      </li>
      <li>
        <a
          href="https://github.com/vuejs/vue-devtools#vue-devtools"
          target="_blank"
          rel="noopener"
          >vue-devtools</a
        >
      </li>
      <li>
        <a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener"
          >vue-loader</a
        >
      </li>
      <li>
        <div @click="exportToExcel">awesome-vue</div>
      </li>
    </ul>
  </div>
</template>

<script>
import ExcelJS from "exceljs";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      test: [
        {
          employee_id: 1,
          first_name:
            "Quyết định - Quyết định phê duyệt Đề cương và dự toán chi tiết Chương trình: Gia hạn bản quyền Hệ thống phòng chống mã độc tập trung - 00005/2023/TTTT-CNTTĐT",
          last_name: "Pettinger",
          age: 77,
          email: "vpettinger0@oaic.gov.au",
          country: "Argentina",
          postal_code: "4178",
          favorite_color: "blue",
          hire_date: "11/17/2009",
          salary: 17515.81,
        },
        {
          employee_id: 2,
          first_name: "Maris",
          last_name: "Gallemore",
          age: 47,
          email: "mgallemore1@scribd.com",
          country: "Indonesia",
          postal_code: null,
          favorite_color: "blue",
          hire_date: "2/28/2021",
          salary: 435590.88,
        },
        {
          employee_id: 3,
          first_name: "Nari",
          last_name: "Tupper",
          age: 33,
          email: "ntupper2@domainmarket.com",
          country: "China",
          postal_code: null,
          favorite_color: "red",
          hire_date: "6/12/2013",
          salary: 146122.8,
        },
        {
          employee_id: 4,
          first_name: "Claude",
          last_name: "Le Strange",
          age: 27,
          email: "clestrange3@independent.co.uk",
          country: "Philippines",
          postal_code: "8303",
          favorite_color: "blue",
          hire_date: "10/27/2012",
          salary: 372906.69,
        },
        {
          employee_id: 5,
          first_name: "Dion",
          last_name: "Kane",
          age: 78,
          email: "dkane4@mashable.com",
          country: "China",
          postal_code: null,
          favorite_color: "blue",
          hire_date: "3/4/2022",
          salary: 337286.85,
        },
        {
          employee_id: 6,
          first_name: "Burtie",
          last_name: "Cushion",
          age: 33,
          email: "bcushion5@nasa.gov",
          country: "Philippines",
          postal_code: "5410",
          favorite_color: "red",
          hire_date: "1/10/2007",
          salary: 386305.18,
        },
        {
          employee_id: 7,
          first_name: "Livvy",
          last_name: "Small",
          age: 50,
          email: "lsmall6@scribd.com",
          country: "Mexico",
          postal_code: "40977",
          favorite_color: "blue",
          hire_date: "6/12/2021",
          salary: 258362.63,
        },
        {
          employee_id: 8,
          first_name: "Maddie",
          last_name: "Mirfin",
          age: 82,
          email: "mmirfin7@constantcontact.com",
          country: "United States",
          postal_code: "71115",
          favorite_color: "red",
          hire_date: "12/12/2008",
          salary: 385899.08,
        },
        {
          employee_id: 9,
          first_name: "Dorie",
          last_name: "Maffiotti",
          age: 22,
          email: "dmaffiotti8@surveymonkey.com",
          country: "Vietnam",
          postal_code: null,
          favorite_color: "red",
          hire_date: "9/4/2002",
          salary: 57110.0,
        },
        {
          employee_id: 10,
          first_name: "Emmeline",
          last_name: "Truelock",
          age: 73,
          email: "etruelock9@chronoengine.com",
          country: "Uzbekistan",
          postal_code: null,
          favorite_color: "blue",
          hire_date: "1/30/2019",
          salary: 300514.12,
        },
        {
          employee_id: 11,
          first_name: "Linnie",
          last_name: "Oblein",
          age: 29,
          email: "lobleina@tuttocitta.it",
          country: "Russia",
          postal_code: "142507",
          favorite_color: "green",
          hire_date: "6/10/2012",
          salary: 259749.99,
        },
        {
          employee_id: 12,
          first_name: "Minerva",
          last_name: "Livett",
          age: 51,
          email: "mlivettb@reference.com",
          country: "Sweden",
          postal_code: "239 30",
          favorite_color: "green",
          hire_date: "7/31/2003",
          salary: 391094.18,
        },
        {
          employee_id: 13,
          first_name: "Roy",
          last_name: "Iorizzi",
          age: 66,
          email: "riorizzic@reddit.com",
          country: "Poland",
          postal_code: "38-507",
          favorite_color: "blue",
          hire_date: "7/17/2012",
          salary: 216062.92,
        },
        {
          employee_id: 14,
          first_name: "Cleavland",
          last_name: "Bedome",
          age: 39,
          email: "cbedomed@ucla.edu",
          country: "Myanmar",
          postal_code: null,
          favorite_color: "red",
          hire_date: "8/19/2022",
          salary: 841532.35,
        },
        {
          employee_id: 15,
          first_name: "Mendy",
          last_name: "Meriton",
          age: 24,
          email: "mmeritone@hhs.gov",
          country: "China",
          postal_code: null,
          favorite_color: "red",
          hire_date: "7/18/2022",
          salary: 904634.27,
        },
        {
          employee_id: 16,
          first_name: "Caesar",
          last_name: "Ancliff",
          age: 83,
          email: "canclifff@sina.com.cn",
          country: "Brazil",
          postal_code: "57120-000",
          favorite_color: "green",
          hire_date: "8/26/2005",
          salary: 684964.28,
        },
        {
          employee_id: 17,
          first_name: "Any",
          last_name: "Di Frisco",
          age: 57,
          email: "adifriscog@pen.io",
          country: "Mexico",
          postal_code: "49274",
          favorite_color: "red",
          hire_date: "5/29/2007",
          salary: 546697.21,
        },
        {
          employee_id: 18,
          first_name: "Albie",
          last_name: "Finlow",
          age: 47,
          email: "afinlowh@cnn.com",
          country: "Burkina Faso",
          postal_code: null,
          favorite_color: "green",
          hire_date: "4/8/2014",
          salary: 809758.45,
        },
        {
          employee_id: 19,
          first_name: "Minette",
          last_name: "Sellick",
          age: 37,
          email: "msellicki@theatlantic.com",
          country: "Indonesia",
          postal_code: null,
          favorite_color: "red",
          hire_date: "11/5/2013",
          salary: 174536.01,
        },
        {
          employee_id: 20,
          first_name: "Hinda",
          last_name: "Covelle",
          age: 75,
          email: "hcovellej@joomla.org",
          country: "Portugal",
          postal_code: "2730-060",
          favorite_color: "green",
          hire_date: "5/28/2015",
          salary: 95982.66,
        },
        {
          employee_id: 21,
          first_name: "Niven",
          last_name: "Eisenberg",
          age: 79,
          email: "neisenbergk@flavors.me",
          country: "China",
          postal_code: null,
          favorite_color: "blue",
          hire_date: "3/14/2001",
          salary: 199988.84,
        },
        {
          employee_id: 22,
          first_name: "Zabrina",
          last_name: "Nyles",
          age: 20,
          email: "znylesl@creativecommons.org",
          country: "United States",
          postal_code: "20067",
          favorite_color: "red",
          hire_date: "5/9/2017",
          salary: 913874.11,
        },
        {
          employee_id: 23,
          first_name: "Sam",
          last_name: "Gerrelt",
          age: 23,
          email: "sgerreltm@networksolutions.com",
          country: "Spain",
          postal_code: "28904",
          favorite_color: "blue",
          hire_date: "6/20/2001",
          salary: 229318.77,
        },
        {
          employee_id: 24,
          first_name: "Algernon",
          last_name: "Piggrem",
          age: 42,
          email: "apiggremn@slate.com",
          country: "China",
          postal_code: null,
          favorite_color: "green",
          hire_date: "6/23/2016",
          salary: 677548.86,
        },
        {
          employee_id: 25,
          first_name: "Urban",
          last_name: "Jedrzejczak",
          age: 53,
          email: "ujedrzejczako@unblog.fr",
          country: "Philippines",
          postal_code: "7104",
          favorite_color: "blue",
          hire_date: "10/3/2020",
          salary: 293115.59,
        },
        {
          employee_id: 26,
          first_name: "Alyce",
          last_name: "Simes",
          age: 32,
          email: "asimesp@blinklist.com",
          country: "Czech Republic",
          postal_code: "273 01",
          favorite_color: "green",
          hire_date: "1/18/2013",
          salary: 634726.62,
        },
        {
          employee_id: 27,
          first_name: "Demetris",
          last_name: "Polotti",
          age: 19,
          email: "dpolottiq@ow.ly",
          country: "Japan",
          postal_code: "329-1117",
          favorite_color: "green",
          hire_date: "6/1/2006",
          salary: 495995.64,
        },
        {
          employee_id: 28,
          first_name: "Natty",
          last_name: "Hebron",
          age: 43,
          email: "nhebronr@wikispaces.com",
          country: "Greece",
          postal_code: null,
          favorite_color: "blue",
          hire_date: "6/2/2017",
          salary: 643819.54,
        },
        {
          employee_id: 29,
          first_name: "Kareem",
          last_name: "O'Drought",
          age: 32,
          email: "kodroughts@discuz.net",
          country: "China",
          postal_code: null,
          favorite_color: "red",
          hire_date: "8/15/2008",
          salary: 669278.05,
        },
        {
          employee_id: 30,
          first_name: "Major",
          last_name: "Huckett",
          age: 32,
          email: "mhuckettt@hhs.gov",
          country: "Brazil",
          postal_code: "57900-000",
          favorite_color: "blue",
          hire_date: "9/13/2008",
          salary: 767326.39,
        },
      ],
    };
  },
  methods: {
    formatJson(filterVal, jsonData) {
      return jsonData.map((v) =>
        filterVal.map((j) => {
          return v[j];
        })
      );
    },
    exportToExcel() {
      // Create a new ExcelJS workbook
      const workbook = new ExcelJS.Workbook();
      const worksheet = workbook.addWorksheet("Sheet 1");

      // Define styles for table header
      const headerStyle = {
        font: {
          bold: true,
          color: { argb: "FFFFFF" }, // White color
        },
        fill: {
          type: "pattern",
          pattern: "solid",
          fgColor: { argb: "0070C0" }, // Blue color
        },
        alignment: {
          horizontal: "center",
        },
        border: {
          top: { style: "thin", color: { argb: "000000" } }, // Black color
          left: { style: "thin", color: { argb: "000000" } },
          bottom: { style: "thin", color: { argb: "000000" } },
          right: { style: "thin", color: { argb: "000000" } },
        },
      };

      // Define style for table data
      const cellStyle = {
        border: {
          top: { style: "thin", color: { argb: "000000" } }, // Black color
          left: { style: "thin", color: { argb: "000000" } },
          bottom: { style: "thin", color: { argb: "000000" } },
          right: { style: "thin", color: { argb: "000000" } },
        },
        alignment: {
          horizontal: "center",
        },
      };
      // Add data to the worksheet

      const data = this.formatJson(
        ["employee_id", "first_name", "last_name", "age", "hire_date"],
        this.test
      );
      data.forEach((row, rowIndex) => {
        row.forEach((cellValue, colIndex) => {
          const cell = worksheet.getCell(rowIndex + 1, colIndex + 1);
          cell.value = cellValue;
          if (rowIndex === 0) {
            // Apply header styles to the first row
            cell.fill = headerStyle.fill;
            cell.font = headerStyle.font;
            cell.alignment = headerStyle.alignment;
            cell.border = headerStyle.border;
          } else {
            // Apply cell styles to data rows
            cell.border = cellStyle.border;
            cell.alignment = cellStyle.alignment;
          }
        });
      });

      // Calculate and set column widths automatically based on content
      worksheet.columns.forEach((column, colIndex) => {
        let maxContentWidth = 10;

        worksheet.eachRow((row) => {
          const cell = row.getCell(colIndex + 1);
          if (cell && cell.value !== null && cell.value !== undefined) {
            const cellWidth = cell.value.toString().length;
            maxContentWidth = Math.max(maxContentWidth, cellWidth);
          }
        });

        // Add some extra padding (e.g., 2 units) to improve readability
        column.width = maxContentWidth + 2;
      });
      
      // Generate a blob from the workbook
      workbook.xlsx.writeBuffer().then((buffer) => {
        const blob = new Blob([buffer], {
          type: "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
        });

        // Create a download link and trigger a click event to download the file
        const link = document.createElement("a");
        link.href = window.URL.createObjectURL(blob);
        link.download = "example.xlsx";
        link.click();
      });
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

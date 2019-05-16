<template>
  <div>
    <a-table
      :rowKey="record => record.id"
      :columns="columns"
      :dataSource="data"
      :pagination="true"
      :loading="loading"
    ></a-table>
  </div>
</template>
<script>
const columns = [
  {
    title: "author_id",
    dataIndex: "author_id",
    width: "20%"
  },
  {
    title: "create_at",
    dataIndex: "create_at",
    width: "20%"
  },

  {
    title: "visit_count",
    dataIndex: "visit_count",
    width: "20%"
  },
  {
    title: "title",
    dataIndex: "title",
    width: "20%"
  },
  {
    title: "reply_count",
    dataIndex: "reply_count",
    width: "20%"
  }
];

export default {
  mounted() {
    this.fetch();
  },
  data() {
    return {
      data: [],
      loading: false,
      columns
    };
  },
  methods: {
    fetch(params = {}) {
      console.log("params:", params);
      this.loading = true;
      this.$http({
        url: "https://cnodejs.org/api/v1/topics",
        method: "get",
        params: {
          page: 1,
          limit: 20
        }
      }).then(data => {
        this.loading = false;
        this.data = data.data.data;
      });
    }
  }
};
</script>
<template>
<div>
   <el-table
      :data="ResultListData"
      style="width: 100%">
      <el-table-column
        prop="Triple.HeadEntity"
        label="HeadEntity">
      </el-table-column>
      <el-table-column
        prop="Triple.Relation"
        label="Relation">
      </el-table-column>
      <el-table-column
        prop="Triple.TailEntity"
        label="TailEntity">
      </el-table-column>
      <el-table-column
        prop="SentenceStructure"
        label="SentenceStructure">
      </el-table-column>
      <el-table-column
        label="Score">
        <template slot-scope="scope">
          <Score :ScoreData="scope.row.score" />
        </template>
      </el-table-column>
    </el-table>
</div>
</template>

<script>
/* eslint-disable */
import Score from "./Score";

export default {
  name: "ResultList",
  components: {
    Score
  },
  props: ["ResultListData"],
  data() {
    return {};
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

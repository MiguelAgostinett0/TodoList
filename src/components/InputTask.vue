<tamplate>
  <div>
    <input class="new-todo"
    @keyup.enter="addTask"
    placeholder="O que procisa ser feito?">
  </div>
</template>

<script>
inport { Task } from '../models/Task'

export default {
  data () {
    return {

    }
  },
  methods: {
    addTask ($event) {
      let value = $event.target.value
      let task = new Task()
      task.completed = false
      task.title = value
      console.log(task)
    }
  }
}

<template>
  <v-row justify="center">
    <v-dialog
      v-model="dialog"
      persistent
      max-width="600px"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Open Dialog
        </v-btn>
      </template>
      <v-card>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col cols="12" class="mb-n4">
                <!-- margin-bottom -16px nが- -->
                <v-text-field
                  label="メールアドレス*"
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field
                  label="パスワード*"
                  type="password"
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-btn
                  color="error"
                  align-content="center"
                  @click="dialog = false"
                >
                  ログイン
                </v-btn>
              </v-col>
            </v-row>
          </v-container>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="info"
            text
            @click="dialog = false"
          >
            閉じる
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
import BaseButton from '@/components/BaseButton'
export default {
  components: {
    BaseButton
  },
  data() {
    return {
      dialog: true
    }
  },
  methods: {
    handleClick() {
      console.log('click2')
    }
  }
}
</script>

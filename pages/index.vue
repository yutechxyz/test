<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" persistent max-width="400px">
      <v-card>
        <v-card-title>
          <v-row justify="center">
            Foot-Repo(ロゴ)
          </v-row>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col cols="12" class="mb-n4">
                <!-- margin-bottom -16px nが- -->
                <!-- メールアドレスのフィールドはバリデーションが必要なので別コンポにする -->
                <v-text-field
                  label="メールアドレス*"
                  type="email"
                  required
                  v-model="email"
                />
              </v-col>
              <v-col cols="12">
                <v-text-field
                  label="パスワード*"
                  type="password"
                  required
                  v-model="pass"
                />
              </v-col>
              <v-row justify="center" class="mt-4">
                <v-col cols="8">
                  <v-btn
                    color="error"
                    block
                    @click="loading = !loading"
                    :loading="loading"
                  >
                    ログイン
                  </v-btn>
                </v-col>
              </v-row>
            </v-row>
          </v-container>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
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
      dialog: true,
      loading: false,
      email: '',
      pass: ''
    }
  },
  methods: {
    handleClick() {
      console.log('click2')
    }
  }
}
</script>

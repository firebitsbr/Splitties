# Alert Dialog Material

*Create simple alert dialogs in material design with simple code*

Supported platforms: **Android**.

## Example

```kotlin
import splitties.alertdialog.material.materialAlertDialog
import splitties.alertdialog.appcompat.cancelButton
import splitties.alertdialog.appcompat.messageResource
import splitties.alertdialog.appcompat.okButton
import splitties.alertdialog.appcompat.onShow
import splitties.alertdialog.appcompat.positiveButton

class YourActivity : AppCompatActivity {

    //...

    private fun doIrreversibleStuffOrCancel() {
        materialAlertDialog {
            messageResource = R.string.dialog_msg_confirm_irreversible_stuff
            okButton { irreversibleStuff() }
            cancelButton()
        }.onShow {
            positiveButton.textColorResource = R.color.red_500
        }.show()
    }
}
```

## Download

```groovy
implementation("com.louiscad.splitties:splitties-alertdialog-material:$splitties_version")
```

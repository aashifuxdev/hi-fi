---
description: The building blocks that make up the Hi-Fi interface.
icon: cubes
---

# Components

Hi-Fi's UI is built from small, reusable components. Each one lives in `src/components/` in its own folder.

## Button

{% code title="Usage" %}
```jsx
<Button variant="primary" onClick={save}>Save</Button>
```
{% endcode %}

| Prop       | Type                                  | Default     |
| ---------- | ------------------------------------- | ----------- |
| `variant`  | `"primary" \| "secondary" \| "ghost"` | `"primary"` |
| `disabled` | `boolean`                             | `false`     |
| `onClick`  | `() => void`                          | —           |

## Card

{% code title="Usage" %}
```jsx
<Card title="Revenue">
  <p>$12,400</p>
</Card>
```
{% endcode %}

## Modal

<details>

<summary>Show Modal example</summary>

```jsx
<Modal open={isOpen} onClose={() => setOpen(false)} title="Confirm">
  Are you sure?
</Modal>
```

</details>

{% hint style="success" %}
All components support light and dark themes out of the box.
{% endhint %}

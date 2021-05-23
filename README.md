Dự án 1:BaiTapHeDIeuHanh
Bài 1: Chỉnh sửa hàm timer_sleep () trong timer.c để chặn hàm trong thời gian ngủ. Create Hàm Wakeup để gọi các chuỗi đang ngủ dậy. Chỉnh sửa hàm timer_interrupt () bằng cách gọi hàm Wakeup thông qua foreach để duyệt ready_list và đánh thức các chức năng cần chỉnh sửa chuỗi cấu trúc trong thread.h hàm: thêm vào tick_blocked biến. This value sẽ thay đổi khi gọi timer_sleep và giảm đi 1 khi timer_interrupt xảy ra. Khi this value down down 0, thì gọi là Wakeup function

Bài 2: Chỉnh sửa file thread.c: Thêm các hàm thread_cmp_priasty (), thread_donate_priasty (), thread_hold_lock (), thread_remove_lock (), lock_cmp_priasty (), thread_update_priasty (). Edit thread_create (), thread_unblock (), thread_set_priasty (), thread_get_priasty (), thread_yield (), init_thread () Chỉnh sửa file synch.c: Edit the sema_up (), sema_down (), lock_acquire (), lock_release ( ), cond_cmp_priasty () Chỉnh sửa file thread.h: Thêm base_priasty biến, struct lock_holding và struct lock_seeking vào trong struct thread Chỉnh sửa file synch.h: add struct elem và variable lock_priasty vào trong struct lock, thêm cond_cmp_priasty ()

Bài 3:

Chỉnh sửa file thread.c: Add thread_get_nice (), thread_set_nice (), thread_get_recent_cpu (), thread_get_load_avg (), mlfqs_inc_recent_cpu (), mlfqs_update_priload_avg_and_recent_cpu file mới thread.h
